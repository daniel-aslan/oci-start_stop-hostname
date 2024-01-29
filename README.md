# OCI-START_STOP-HOSTNAMES

Description
This is to setup plays to turn off and on instances in Oracle Cloud by hostnames on a schedule.

## Installation / Usage
Instance hostnames and ocid's will be stored in the variables file 'all.yaml' , under the 'group_vars' directory in the root directory.
Initially all hostnames will be commented out.
When making exceptions to the instances that need to be updated simply pull the repo and update the hostnames under their respective compartment names in the all.yaml folder, Create a commit with your initials and reason for change. Then push the changes back to the repo and AWX should pull the changes on its next run.

When running this from AWX ensure that the execution enviroment is used with the appropriate OCI config for the tenancy that this is to be applied to also ensure that the EE has the OCI SDK installed.

Tags will be used to specify start or stop roles.

```bash
ansible-playbook site.yml --tags start
```

or

```bash
ansible-playbook site.yml --tags stop
```



###### Daniel Aslan
###### daniel.aslan@outlook.com
