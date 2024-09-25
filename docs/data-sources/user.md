---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailscale_user Data Source - terraform-provider-tailscale"
subcategory: ""
description: |-
  The user data source describes a single user in a tailnet
---

# tailscale_user (Data Source)

The user data source describes a single user in a tailnet

## Example Usage

```terraform
data "tailscale_user" "32571345" {
  id = 32571345
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `id` (String) The unique identifier for the user.
- `login_name` (String) The emailish login name of the user.

### Read-Only

- `created` (String) The time the user joined their tailnet.
- `currently_connected` (Boolean) true when the user has a node currently connected to the control server.
- `device_count` (Number) Number of devices the user owns.
- `display_name` (String) The name of the user.
- `last_seen` (String) The later of either: a) The last time any of the user's nodes were connected to the network or b) The last time the user authenticated to any tailscale service, including the admin panel.
- `profile_pic_url` (String) The profile pic URL for the user.
- `role` (String) The role of the user.
- `status` (String) The status of the user.
- `tailnet_id` (String) The tailnet that owns the user.
- `type` (String) The type of relation this user has to the tailnet associated with the request.