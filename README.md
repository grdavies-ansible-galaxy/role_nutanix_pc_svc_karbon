# Nutanix Role to manage the Karbon service within Prism Central

This Ansible role manage the Karbon service within Prism Central.

## Role Variables

| Variable                                          | Required | Default | Choices                   | Comments                                                                                               |
|---------------------------------------------------|----------|---------|---------------------------|--------------------------------------------------------------------------------------------------------|
| nutanix_host                                      | yes      |         |                           | The IP address or FQDN for the Prism Centra) where you want to enable the service.                     |
| nutanix_username                                  | no       | "admin" |                           | A valid username with appropriate rights to access the Nutanix API.                                    |
| nutanix_password                                  | yes      |         |                           | A valid password for the supplied username.                                                            |
| nutanix_port                                      | no       | 9440    |                           | The Prism TCP port                                                                                     |
| validate_certs                                    | no       | false   | true / false              | Whether to check if Prism UI certificates are valid.                                                   |
| nutanix_debug                                     | no       | false   | true / false              | Whether to output variable contents for debugging purposes.                                            |
| nutanix_karbon_enable                             | yes      | false   | true / false              | Set to 'true' to enable Karbon.                                                                        |
| nutanix_karbon_download_images                    | yes      | false   | true / false              | Set to 'true' to download the Karbon OS image(s).                                                      |

## Dependencies

None

## Example Playbook

```YAML
- hosts: localhost
  gather_facts: false
  roles:
    - role: grdavies.role_nutanix_pc_svc_karbon
  vars:
    nutanix_host: 10.38.179.39
    nutanix_username: admin
    nutanix_password: nx2Tech283!
    nutanix_karbon_enable: yes
    nutanix_karbon_download_images: yes
```

## License

See LICENSE.md

## Author Information

Ross Davies
