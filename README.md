# Cloud-Foundry-DRS


resource_pools:
- cloud_properties:
    cpu: 2
    disk: 32768
    ram: 16384
  env:
    bosh:
      password: REDACTED
  name: runner_z1
  network: cf1
  stemcell:
    name: bosh-vsphere-esxi-ubuntu-trusty-go_agent
    version: latest
    
    


resource_pools:
- name: hadoop-datanodes
  cloud_properties:
    datacenters:
    - name: my-dc
      clusters:
      - my-vsphere-cluster:
          drs_rules:
          - name: separate-hadoop-datanodes-rule
            type: separate_vms
