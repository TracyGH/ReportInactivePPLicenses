# Report Inactive Power Platform Premium (user) Licenses
Power Automate flow for Reporting Inactive** Premium/Per-User Power Platform Licenses

### Become your organization's hero 🦸 by saving them some $$$ 💵 in Microsoft licensing fees!

#### 1. Download the _InactivePremiumPowerAutomateLicenses_20241022192410.zip_ file and import as Legacy Power Automate flow package.

<kbd> ![image](https://github.com/user-attachments/assets/c09b3f6e-b2da-472b-8adc-ce4fc81634a9) </kbd>
#### 2. For the first connection resource, create a new HTTP with Microsoft Entra ID (preauthorized) connection and set the Base URL and Resource URI to `https://licensing.powerplatform.microsoft.com`
> [!NOTE]
> GCC tenants will use `https://gov.licensing.powerplatform.microsoft.us`

<kbd>![image](https://github.com/user-attachments/assets/00b94e6f-ae29-4194-b721-c91eb3563924)</kbd>

<kbd>![image](https://github.com/user-attachments/assets/89533526-1ddc-4c26-8f00-796c5f177341)</kbd>

#### 3. Repeat for the second connection resource setting the Base URL and Resource URI to `https://graph.microsoft.com`

#### 4. Once imported, edit the _Get Active Power Automate Premium Users_ action and update the Url with your respective Tenant Id.
<kbd>![image](https://github.com/user-attachments/assets/64349b18-dc73-4ed0-b2ae-cb0140fa624d)</kbd>

#### 5. Next, edit the Get All Power Automate Premium Users action and update the Url with [your respective license SKU](#getLicenseSKU).
<kbd>![image](https://github.com/user-attachments/assets/6e77d652-c76e-4cc7-a1ac-e504b32fd142)</kbd>






<a name="getLicenseSKU"></a>
| License Type | Commercial Tenant SKU | GCC Tenant SKU |
| --- | --- | --- |
| Power Automate (per user) Premium | eda1941c-3c4f-4995-b5eb-e85a42175ab9 | d3987516-4b53-4dc0-8335-411260bf5626 |
| Power Apps (per user) Premium | b30411f5-fea1-4a59-9ad9-3db7c7ead579 | 8e4c6baa-f2ff-4884-9c38-93785d0d7ba1 |

> [!NOTE]
> These values may periodically change and the latest can be found [here](https://learn.microsoft.com/en-us/entra/identity/users/licensing-service-plan-reference) and [here](https://download.microsoft.com/download/e/3/e/e3e9faf2-f28b-490a-9ada-c6089a1fc5b0/Product%20names%20and%20service%20plan%20identifiers%20for%20licensing.csv).

> [!NOTE]
> This flow will only report inactive** [Power Automate Premium licenses, not inactive** Power Automate per user with attended RPS license](https://learn.microsoft.com/en-us/power-platform/admin/power-automate-licensing/faqs#how-is-power-automate-premium-license-different-from-power-automate-per-user-with-attended-rpa-license). 



