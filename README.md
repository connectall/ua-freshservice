# ua-freshservice

The ConnectALL Freshservice Universal Adapter is developed as an extension to the universal adapter capability of ConnectALL. This adapter will allow the user to use Freshservice with ConnectALL. Current capabilities and limitations will be defined below.

Please refer to the [ConnectALL Tech Docs](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/connectall/3-8/adapters/universal-adapter.html) for more information on the ConnectALL Universal Adapter.

If you are an existing SaaS customer, please contact Broadcom Support to enable the adapter in your environment. If you are using ConnectALL On-Premise, you may download and install this adapter in your environment. If you are not yet a customer, [please reach out to learn more](https://enterprise-software.broadcom.com/contact-us).

# Setup

## Supported Entities

This Universal Adapter currently supports the following entities:
* Incident

*Note: This Universal Adapter is provided as-is. It is tested and validated using the entities and configurations as defined. Any additional customizations are not supported and should be made at your own discretion.*

## Connection Details
Authentication to Freshservice is supported using basic authentication. A generated API key is used as a username and a password must also be provided. See the [Freshservice API Authenticaiton](https://api.freshservice.com/#authentication) documentation for more info.
* **Connection Name:** *Name of Application*
* **Application Type:** *freshservice*
* **URL:** *Base URL for application API (ex: https://yourdomain.freshservice.com)*
* **User Name:** *Generated API Token*
* **Password:** *Your Password*
* **Application Category:** *Select from dropdown list*
* **Time Zone:** *Not Required*
* **Select Group:** *Select Group if neccessary*
* **Auth Option:** *Header*
* **Authentication Type:** *Basic*
* **API Key:** *Leave Blank*
* **API Value:** *Leave Blank*

## Flow Filters

Flow filters have not been implemented for this Universal Adapter.

## Example Automation

*Sync Incidents from Freshservice to Rally as Defects.*

# Known Limitations

* Attachments cannot be supported because there is no unique URL for fetching attachments.
* Mandatory fields for creation are Subject, Description, Status, Priority, and one of [requestor_id (integer), phone (integer), or email (string)].
* Developer note: "The tricky mandatory field is phone, if you give a "phone": 5551234567, then you have to mention another field 'name': 'Anyname' in the request."

# Supporting Documentation

Third Party API Documentation: [Freshservice API Documentation](https://api.freshservice.com/)
