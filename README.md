
# Reference Application: Efimis and iManage Integration

## Overview

This application serves as a **reference integration** between **Efimis** (a web application for legal accounts management) and **iManage** (a document management system). It demonstrates key capabilities for reacting to events in Efimis and interacting with iManage to update entities and manage document uploads.

---

## Features

### Webhook Management
- Registering webhooks for events occurring in Efimis.
- Handling received webhook messages.

### API Interaction
- Fetching client, matter and document data from Efimis' API.

### Tenant Configuration
- Enabling a single application instance to handle multiple tenants at once.

### Integration with iManage
- Uploading documents triggered by Efimis events to iManage.
- Synchronizing entity updates across systems.

---

## Requirements

- **Efimis API access**: Ensure your Efimis instance has webhooks and API features enabled.
- **iManage API credentials**: Obtain valid API keys and configuration for iManage.

---

## Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/efimis-dev/efimis-imanage-integration
   ```

2. **Configure Dev Environment**
   - Edit appsettings.development.json with values specific to your Efimis and iManage dev systems.
	- Settings are documented in appsettings.json.
	- Base Efimis settings are at the top level of the config file.
	- Tenant-specific details are in the 'Tenants' array.

3. **Run the Application**
   Launch the application:
   - F5 in Visual Studio

4. **Deploy**
   Deploy into a web hosting service of your choice.
---

## Usage
1. Run app with and observe webhooks being registered in Efimis.
2. Open Efimis and Create/Modify Clients and Matters and add documents to Matters.
3. Observe webhook callbacks into PrimeController and commands invoked on Efimis Api and iManage.
4. Open iManage browser and observe Workspaces that have been created for the Matter and documents that have been added within with correct Client and Matter attributes.
