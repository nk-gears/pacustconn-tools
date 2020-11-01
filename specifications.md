# Power Automate Custom Connector - Build Tool

All Definitions will be Placed in the pacc.yml file
- pacc.json


We will have the following actions for the CLI

- pacc init 
- pacc create
- pacc pull
- pacc push
- pacc validate

## pacc init 
- Creates a New Custom Connector with the Basic Setup Locally
- Creates a New Folder in the root of the connector

```
├── connector_1
│   ├── base
│   │   ├── apiDefinition.swagger.json
│   │   ├── apiProperties.json
│   │   └── icon.png
│   ├── build
│   │   ├── apiDefinition.swagger.json
│   │   ├── apiProperties.json
│   │   └── icon.png
│   ├── partials
│   └── properties
├── connector_2
└── connector_3
```

## pacc create 
- Creates a New action to the default Connector
- Supported options
  - method -m GET, POST, PATCH,DELETE
  - action Name -A : This will be used as Operation Id

## pacc pull 
- Creates a New Custom Connector Locally by Importing from the remote PA
- Supported Options
  - -g Group by Folders using TagName

## pacc push 
- Publishes a New Custom Connector Remotely 
- Options Supported 
  - -e environment name
```
  pacc push connectorName -e dev
```  

## pacc validate 
- Validates the Swagger file using paconn validate