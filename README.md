# Azure Partner center GitHub action

This action update the artifact of a plan within the Solution Template offer.

## Prerequisites

To have the action works, you will need to setup three repository secrets for your pipeline(you can also pass them as parameters but it is not recommended):

* CLIENT_ID: Client ID for an Azure AD application.
* SECRET_VALUE: Secret value of the application.
* TENANT_ID: Tenant ID you'd like to run pipeline against.

Here are the steps to get those credentials:

1. [Complete prerequisites for using the Partner Center submission API](https://learn.microsoft.com/en-us/azure/marketplace/azure-app-apis#how-to-associate-an-azure-ad-application-with-your-partner-center-account).

1. [Quickstart: Register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app#changing-the-application-registration-to-support-multi-tenant)

1. [Associate an existing Azure AD tenant with your Partner Center account](https://learn.microsoft.com/en-us/windows/apps/publish/partner-center/associate-existing-azure-ad-tenant-with-partner-center-account).

## Inputs

### `offerName`

**Required** The name of the offer.

### `planName`

**Required** The name of the plan.

### `filePath`

**Required** The path to the artifact(ZIP file).

### `artifactVersion`

**Required** The new version of the artifact.

### `clientId`

**Required** Client ID for an Azure AD application.

### `secretValue`

**Required** Secret value of the application.

### `tenantId`

**Required** Tenant ID you'd like to run pipeline against.

## Outputs

## Example usage

```terminal
uses: zhengchang907/microsoft-partner-center-action@v1
with:
  offerName: offerName
  planName: planName
  filePath: filePath
  artifactVersion: artifactVersion
  clientId: clientId
  secretValue: secretValue
  tenantId: tenantId
```