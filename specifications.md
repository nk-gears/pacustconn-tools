# Power Automate Custom Connector - Build Tool


## How this tools works

- The tool will be published as a npm package
- The user will be simply installs the pacustconn package from NPM as a global cli
- The CLI exposes few commands to automate the process of creating connectors, adding actions to a connector
- Connectors are organized under multiple folders. So, we can manage single or multiple connectors in a project


All configurations will be placed in the pacc.json

We will have the following actions for the CLI

- pacc init 
- pacc create
- pacc build
- pacc validate
- pacc pull
- pacc push


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


## pacc build 
- Builds the final the Swagger file using paconn validate

## pacc validate 
- Validates the Swagger file using paconn validate

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

## Library/Tool Dependencies

Need to get Nick's Suggestions as well

- paconn - Official custom library
- commander - NodeJS command line Utility. The next alternate option is using chalk.
