### Overview

### DWAPI(Data Warehouse API)
This is a web-based API tool developed by KeHMIS team. DWAPI is installed at the EMR implementing facilities and extracts data from EMR databases, runs de-duplication and data quality routines before securely transmitting the extract to an API at NDW staging area for further processing. Read full documentation [here](https://kenyahmis.org/documentation/summary-national-data-warehouse/)

See [manual installation](https://hub.docker.com/r/kenyahmis/dwapi)


### dwapi_deploy
This playbook deploys a dwapi instance on specified host(s).

### Run below command to deploy dwapi on a test instances:

`ansible-playbook -i inventory -l test dwapi.yml --ask-become --ask-vault-pass -vvv`

### Encrypt/Decrypt secrets:

`ansible-vault en(de)crypt group_vars/test/vault.yml --ask-vault-pass`