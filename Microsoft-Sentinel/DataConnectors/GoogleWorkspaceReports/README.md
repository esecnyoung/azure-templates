# Google Workspace Sentinel Connector

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fesecnyoung%2Fazure-templates%2Fmain%2FMicrosoft-Sentinel%2FDataConnectors%2FGoogleWorkspaceReports%2FGoogleWorkspaceReports.json)

## Parameters

### GooglePickleString

Get your pickled Google Workspace object by running

```bash
pip install google-auth-oauthlib
python get_pickle_string.py
```

*When your browser opens, login with your Google account with Admin reporting access.*

### Audit Log Types

Create a comma separated list of audit log types to be included in the report. Leave blank to include all audit log types.

* access_transparency
* admin
* calendar
* chat
* drive
* gcp
* gplus
* groups
* groups_enterprise
* jamboard
* login
* meet
* mobile
* rules
* saml
* token
* user_accounts
* context_aware_access
* chrome
* data_studio

e.g. `access_transparency,admin,gcp,groups,groups_enterprise,login,meet,mobile,rules,saml,token,user_accounts,context_aware_access,chrome`

### keyVaultGroup

This parameter is optional, it will add an access policy for the supplied principal ID (group or user) to the key vault with permissions:

* backup
* list
* recover
* restore
* set
