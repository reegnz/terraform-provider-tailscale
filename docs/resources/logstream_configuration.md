---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailscale_logstream_configuration Resource - terraform-provider-tailscale"
subcategory: ""
description: |-
  The logstream_configuration resource allows you to configure streaming configuration or network flow logs to a supported security information and event management (SIEM) system. See https://tailscale.com/kb/1255/log-streaming for more information.
---

# tailscale_logstream_configuration (Resource)

The logstream_configuration resource allows you to configure streaming configuration or network flow logs to a supported security information and event management (SIEM) system. See https://tailscale.com/kb/1255/log-streaming for more information.

## Example Usage

```terraform
resource "tailscale_logstream_configuration" "sample_logstream_configuration" {
  log_type         = "configuration"
  destination_type = "panther"
  url              = "https://example.com"
  token            = "some-token"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `destination_type` (String) The type of system to which logs are being streamed.
- `log_type` (String) The type of log that is streamed to this endpoint.
- `token` (String, Sensitive) The token/password with which log streams to this endpoint should be authenticated.
- `url` (String) The URL to which log streams are being posted.

### Optional

- `user` (String) The username with which log streams to this endpoint are authenticated. Only required if destination_type is 'elastic', defaults to 'user' if not set.

### Read-Only

- `id` (String) The ID of this resource.