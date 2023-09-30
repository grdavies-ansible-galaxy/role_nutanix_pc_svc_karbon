# Nutanix Role to manage the Karbon service within Prism Central

This Ansible role manage the Karbon service within Prism Central.

## Input Variables

| Variable                                       | Required | Default | Choices                   | Comments                                                                                               |
|------------------------------------------------|----------|---------|---------------------------|--------------------------------------------------------------------------------------------------------|
| role_nutanix_pc_svc_karbon_host                | yes      |         |                           | The IP address or FQDN for the Prism Centra) where you want to enable the service.                     |
| role_nutanix_pc_svc_karbon_host_username       | no       | "admin" |                           | A valid username with appropriate rights to access the Nutanix API.                                    |
| role_nutanix_pc_svc_karbon_host_password       | yes      |         |                           | A valid password for the supplied username.                                                            |
| role_nutanix_pc_svc_karbon_host_port           | no       | 9440    |                           | The Prism TCP port                                                                                     |
| role_nutanix_pc_svc_karbon_host_validate_certs | no       | false   | true / false              | Whether to check if Prism UI certificates are valid.                                                   |
| role_nutanix_pc_svc_karbon_debug               | no       | false   | true / false              | Whether to output variable contents for debugging purposes.                                            |
| role_nutanix_pc_svc_karbon_enable              | yes      |         | true / false              | Set to 'true' to enable Karbon.                                                                        |
| role_nutanix_pc_svc_karbon_download_images     | yes      |         | true / false              | Set to 'true' to download the Karbon OS image(s).                                                      |

## Dependencies

- grdavies.role_nutanix_prism_api

## Example Playbook

```YAML
- hosts: localhost
  gather_facts: false
  roles:
    - role: grdavies.role_nutanix_pc_svc_karbon
  vars:
    role_nutanix_pc_svc_karbon_host: 10.38.179.39
    role_nutanix_pc_svc_karbon_host_username: admin
    role_nutanix_pc_svc_karbon_host_password: nx2Tech283!
    role_nutanix_pc_svc_karbon_enable: true
    role_nutanix_pc_svc_karbon_download_images: true
```

## License

See LICENSE.md

## Author Information

Ross Davies
