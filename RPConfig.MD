```
- cloud_properties:
    cpu: 2
    disk: 32768
    ram: 16384
    datacenters:
    - name: DC2
      clusters:
      - 'PaaS POC': {resource_pool: Resources}
        drs_rules:
        - name: separate-dea-nodes-rule
          type: separate_vms
  env:
    bosh:
      password: $6$4gDD3aV0rdqlrKC$2axHCxGKIObs6tAmMTqYCspcdvQXh3JJcvWOY2WGb4SrdXtnCyNaWlrf3WEqvYR2MYizEGp3kMmbpwBC6jsHt0
  name: runner_z2
  network: cf2
  stemcell:
    name: bosh-vsphere-esxi-ubuntu-trusty-go_agent
    version: latest
```
