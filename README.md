# APIM
Azure API Management instance using Terraform
azure-apim-repo/
├── modules/
│   ├── apim-instance/        # Creates the base APIM service
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   └── apim-api/             # Reusable module to add new APIs
│       ├── main.tf
│       └── variables.tf
├── environments/
│   ├── dev/
│   │   ├── main.tf           # Deploys instance + APIs
│   │   ├── apis.tf           # API definitions for dev
│   │   └── providers.tf
└── policies/                 # XML files for inbound/outbound logic
    └── global-policy.xml
