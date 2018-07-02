# Description
Use this policy to get a list of applications that are subscribed to your APIs. You get back a JSON-Output with an Array of APIs and inside each an Array with the subscribed aps.
```json
[
    {
        "ce28906f-bff3-4684-a8aa-dfcbb357295e": [
            {
                "id": "7c7c26f9-ddd2-4af0-b85e-4409a5b9795e",
                "name": "FHIR - Everything Health",
                "description": "An application that promotes healthy living.",
                "organizationId": "53437f82-8db5-4f61-9f9b-0b34db8be847",
                "phone": null,
                "email": null,
                "createdBy": "f7289d70-c71b-4c6b-a2bb-9461f93b91aa",
                "managedBy": [],
                "createdOn": 1490382897657,
                "enabled": true,
                "image": "/api/portal/v1.3/applications/7c7c26f9-ddd2-4af0-b85e-4409a5b9795e/image",
                "state": "approved"
            },
            {
                "id": "1a6e666d-2ef2-49c2-97cc-79f7dc8a565d",
                "name": "Plexus Suite – Patient Monitoring",
```

## API Management Version Compatibilty
This artefact was successfully tested for the following versions:
- V7.5.3

## Install
- Import the Policy-Configuration Fragment (api-subscriptions.xml) into your Policy-Studio configuration
- link this policy to a Path on a Listener you want (Example: https://apihost.com:8080/get-api-subscriptions)
- Setup the hostname of your API-Manager in the following Connect to URL filters:
  - Policy: "Generate API-List": "Get List of Applications" & "List of APIs from API-Mgt"
  - Policy: "Get All Subscriptions": "List App-Subscriptions"
- Setup the Client-Credential profile: "API-Manager" with a valid username and password

## Usage
Call the Policy on the configured path. Example: https://apihost.com:8080/get-api-subscriptions

## Bug and Caveats

This Policy has is using a Loop to iterate over all registered applications and has been tested only with a limited number of applications (15). Please use it with care, when having more applications.

## Contributing

Please read [Contributing.md](https://github.com/Axway-API-Management/Common/blob/master/Contributing.md) for details on our code of conduct, and the process for submitting pull requests to us.


## Team

![alt text][Axwaylogo] Axway Team

[Axwaylogo]: https://github.com/Axway-API-Management/Common/blob/master/img/AxwayLogoSmall.png  "Axway logo"


## License
[Apache License 2.0](/LICENSE)
