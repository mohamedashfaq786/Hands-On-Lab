# Okta Hands-On Lab — SAML, SWA & Active Directory Integration

A step-by-step guide to integrating popular applications with Okta using SAML and SWA authentication, plus Active Directory integration.

---

## Table of Contents

1. [Integrating Google Workspace using SAML](#1-integrating-google-workspace-using-saml)
2. [Integrating ServiceNow using SAML](#2-integrating-servicenow-using-saml)
3. [Integrating Atlassian Cloud using SAML](#3-integrating-atlassian-cloud-using-saml)
4. [Integrating Microsoft Azure using SWA](#4-integrating-microsoft-azure-using-swa)
5. [Integrating Active Directory with Okta](#5-integrating-active-directory-with-okta)

---

## 1. Integrating Google Workspace using SAML

**Authentication Type:** SAML (Security Assertion Markup Language)  
**App:** Google Workspace

SAML allows Okta to act as an Identity Provider (IdP). When a user logs into Google Workspace, Okta handles the authentication and sends a SAML assertion to Google.

### Steps

**Step 1** — Log in to your Okta Admin Console and navigate to **Applications → Applications**.

<img width="975" height="534" alt="image" src="https://github.com/user-attachments/assets/d41eae06-651f-4803-bab2-116c24dc4d56" />


**Step 2** — Click **Browse App Catalog** to search for a pre-built integration.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/161e54ee-7e48-45d9-a58f-a2f556d71d96" />


**Step 3** — Search for **Google Workspace** in the catalog and select it.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/32f4cb34-c8a4-49a2-bdf2-9bb192716df1" />


**Step 4** — Click **Add Integration** to begin the setup.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/32f4cb34-c8a4-49a2-bdf2-9bb192716df1" />

**Step 5** — Fill in the **General Settings** for the Google Workspace app (display name, visibility options).

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/c7e465ff-1557-4725-ba8d-2711147e574f" />

**Step 6** — Move to the **Sign-On** tab and select **SAML 2.0** as the sign-on method.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/126b9c66-f739-40f4-85da-158d966432fe" />


**Step 7** — Configure the SAML settings — enter your Google domain details.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4309c80a-dec6-4340-951e-70e3e360e0aa" />


**Step 8** — Under **Credentials Details**, set the Application username format.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4309c80a-dec6-4340-951e-70e3e360e0aa" />

**Step 9** — Note the **Identity Provider metadata** URL (you will need this in Google Admin Console).

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4309c80a-dec6-4340-951e-70e3e360e0aa" />

**Step 10** — Go to the **Assignments** tab and assign the app to users or groups.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4309c80a-dec6-4340-951e-70e3e360e0aa" />

**Step 11** — Log in to the **Google Admin Console** (`admin.google.com`) and navigate to **Security → Authentication → SSO with third-party IdP**.

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/dc0676a3-a394-4f0e-8c51-6ed8964c1aba" />


**Step 12** — Enable SSO and paste in the **SSO URL**, **Entity ID**, and upload the **certificate** from Okta.

<img width="975" height="550" alt="image" src="https://github.com/user-attachments/assets/66ff97c9-70a2-40f5-98fb-cd03715dafbd" />


**Step 13** — Save the configuration in Google Admin Console.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/5dc047dc-786c-4886-9228-03322eb8dd15" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/7dd70c2c-06d6-4fdc-858a-97cbb5a7d346" />


**Step 14** — Back in Okta, verify the integration status shows as active.

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/4daa142c-17be-4acd-b2e4-99370f725df3" />


**Step 15** — Test the integration by accessing Google Workspace from the Okta dashboard.

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/d5631081-2379-4c53-8b8c-3704652ef061" />


**Step 16** — Confirm successful SSO login to Google Workspace.

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/7ce4b371-b734-4355-9e2c-6776ee1ad7f2" />


**Step 17** — Review the sign-on policy settings if needed.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/11335c79-790f-4d4d-a5a3-2a4a321f716b" />

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/de97933e-b655-42f6-8bb4-866d49ed81f7" />



**Step 18** — Optionally configure **Provisioning** to auto-create accounts in Google.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f1eb5c08-69b2-4aff-9a1f-c05f10ecebd5" />

**Step 19** — Enable provisioning features (Create Users, Update Attributes, Deactivate Users).

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/f1eb5c08-69b2-4aff-9a1f-c05f10ecebd5" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/e4f40a04-e89f-4770-ac56-7f886e12f499" />

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/037ff37c-edbb-47c9-960c-fa1b913faeb0" />


**Step 20** — Google Workspace SAML integration is now complete ✅

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/4102fc40-771e-4aae-8337-82aaf3e7788a" />


---

## 2. Integrating ServiceNow using SAML

**Authentication Type:** SAML  
**App:** ServiceNow User Dashboard

### Steps

**Step 1** — In Okta Admin Console, go to **Applications → Browse App Catalog** and search for **ServiceNow**.

<img width="975" height="425" alt="image" src="https://github.com/user-attachments/assets/2db7626d-76aa-4a26-9b2a-05c295bdddcc" />


**Step 2** — Select **ServiceNow** and click **Add Integration**.

<img width="975" height="449" alt="image" src="https://github.com/user-attachments/assets/ae7c6ea3-dc94-4b50-aade-a04da78a7c7a" />


**Step 3** — Enter your ServiceNow instance URL in the General Settings (e.g., `https://yourinstance.service-now.com`).

<img width="975" height="514" alt="image" src="https://github.com/user-attachments/assets/3a7d54c3-3cad-470c-b869-3ce301b17477" />


**Step 4** — On the **Sign-On** tab, select **SAML 2.0**.

<img width="975" height="540" alt="image" src="https://github.com/user-attachments/assets/4e6092b9-4135-49c4-b999-31dc54864170" />


**Step 5** — Copy the **Metadata URL** from Okta — you will paste this in ServiceNow.

<img width="975" height="531" alt="image" src="https://github.com/user-attachments/assets/02939a48-14e9-40c4-bb83-dcc55809fa79" />


**Step 6** — Log in to your **ServiceNow** instance as an admin and navigate to **Multi-Provider SSO → Identity Providers**.

<img width="975" height="516" alt="image" src="https://github.com/user-attachments/assets/6f89d9f4-1ca7-4da1-a218-97d3dea73839" />

<img width="975" height="418" alt="image" src="https://github.com/user-attachments/assets/f3a6804a-3614-4f94-9283-275e879bfba4" />


**Step 7** — Click **New** and choose **SAML** as the type.

<img width="975" height="321" alt="image" src="https://github.com/user-attachments/assets/79015a74-7126-4381-91f3-f9aef44c1bb4" />

<img width="975" height="208" alt="image" src="https://github.com/user-attachments/assets/07e99e51-87c2-4ecb-bef6-e8d432143c26" />

<img width="975" height="228" alt="image" src="https://github.com/user-attachments/assets/0a43322e-bfad-4240-800e-19cca2811b1e" />


**Step 8** — Paste the **Okta Metadata URL** and click **Import**.

<img width="975" height="417" alt="image" src="https://github.com/user-attachments/assets/657586c8-d5d5-4751-8453-708687d889ca" />


**Step 9** — Review the auto-populated SAML settings and save.

<img width="975" height="479" alt="image" src="https://github.com/user-attachments/assets/b272735d-f3c7-4168-9e68-37bda06a383d" />


**Step 10** — Enable the Identity Provider and set it as default (optional).

<img width="975" height="535" alt="image" src="https://github.com/user-attachments/assets/59e6e3a6-fb10-415f-9654-922105b73c0c" />


**Step 11** — Back in Okta, go to the **Assignments** tab and assign users to ServiceNow.

<img width="975" height="510" alt="image" src="https://github.com/user-attachments/assets/a279314a-4458-42d3-b0a3-527a8a7991c2" />


**Step 12** — Test SSO by accessing ServiceNow from the Okta dashboard.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/22a56226-3558-4df7-a523-990ee9197ef7" />


**Step 13** — ServiceNow SAML integration is now complete ✅

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/3c03dd71-7278-4562-9121-d478ac26a991" />

---

## 3. Integrating Atlassian Cloud using SAML

**Authentication Type:** SAML  
**App:** Atlassian Cloud (Jira, Confluence)

### Steps

**Step 1** — In Okta, go to **Applications → Browse App Catalog** and search for **Atlassian Cloud**.

<img width="975" height="430" alt="image" src="https://github.com/user-attachments/assets/db97fa85-af89-4286-99e4-bc6da3c1b14a" />


**Step 2** — Select **Atlassian Cloud** and click **Add Integration**.

<img width="975" height="333" alt="image" src="https://github.com/user-attachments/assets/e82c9aae-43c0-4dbc-a17b-4f2849472cf0" />


**Step 3** — Enter your Atlassian organization details in General Settings.

<img width="975" height="333" alt="image" src="https://github.com/user-attachments/assets/e82c9aae-43c0-4dbc-a17b-4f2849472cf0" />

**Step 4** — On the Sign-On tab, select **SAML 2.0** and copy the Metadata URL.

<img width="975" height="509" alt="image" src="https://github.com/user-attachments/assets/16081e6a-0a06-4c8d-bca8-efe4d4f4a889" />


**Step 5** — Log in to **admin.atlassian.com** → **Security → SAML single sign-on**.

<img width="975" height="548" alt="image" src="https://github.com/user-attachments/assets/4acf6d73-606b-4606-bed4-defae2aa318e" />


**Step 6** — Click **Add SAML configuration** and paste the Okta **SSO URL** and **Certificate**.

<img width="975" height="549" alt="image" src="https://github.com/user-attachments/assets/8e1548ce-1f64-4c02-8a7f-27871381e089" />


**Step 7** — Copy the **SP Entity ID** and **ACS URL** from Atlassian and enter them back in Okta.

<img width="975" height="519" alt="image" src="https://github.com/user-attachments/assets/6849ee00-a3de-4f53-92d9-a3126981d198" />


**Step 8** — Save the SAML configuration in Atlassian Admin.

<img width="975" height="459" alt="image" src="https://github.com/user-attachments/assets/f79b4323-9a61-4a70-ae17-2c3940346e9e" />

<img width="975" height="474" alt="image" src="https://github.com/user-attachments/assets/ac53e6c7-312e-41a3-a5ec-83bfa26c5d21" />

<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/632c059c-bcf6-4abf-a2f4-e06f9a8d9ef6" />

<img width="975" height="452" alt="image" src="https://github.com/user-attachments/assets/a6a899f5-15e8-4f5f-bca0-47f7aada8826" />

<img width="975" height="436" alt="image" src="https://github.com/user-attachments/assets/a8720b03-cf19-4aeb-a632-36341840523f" />


**Step 9** — Back in Okta, assign users or groups to the Atlassian Cloud app.

<img width="975" height="493" alt="image" src="https://github.com/user-attachments/assets/bf9190ed-337b-4095-ac0d-225ff22f36d8" />

<img width="975" height="389" alt="image" src="https://github.com/user-attachments/assets/50392327-9532-4561-959e-1df20b3dd475" />

<img width="975" height="513" alt="image" src="https://github.com/user-attachments/assets/89bb95c7-5c51-48c0-bddd-796ed97fc25f" />

<img width="975" height="534" alt="image" src="https://github.com/user-attachments/assets/0b152582-8ae6-4b55-9c50-4be6ea15989e" />

<img width="975" height="396" alt="image" src="https://github.com/user-attachments/assets/025b839c-aac4-49e3-b57c-5f80d5806141" />

<img width="975" height="406" alt="image" src="https://github.com/user-attachments/assets/729134d9-b152-4e32-93da-2518e73beb7a" />


**Step 10** — Atlassian Cloud SAML + SCIM integration is now complete ✅

<img width="975" height="475" alt="image" src="https://github.com/user-attachments/assets/c751e568-bcee-435c-9ed6-bdae5f8f9bd9" />

---

## 4. Integrating Microsoft Azure using SWA

**Authentication Type:** SWA (Secure Web Authentication)  
**App:** Microsoft Azure

> **What is SWA?** SWA (Secure Web Authentication) is used when an application does not support SAML. Okta securely stores and replays credentials on behalf of the user — like a password manager built into SSO.

### Steps

**Step 1** — In Okta, go to **Applications → Browse App Catalog** and search for **Microsoft Azure**.

<img width="975" height="485" alt="image" src="https://github.com/user-attachments/assets/7766c18f-e73f-424e-814b-f7f5a01adaf2" />


**Step 2** — Select the app and click **Add Integration**.

<img width="975" height="409" alt="image" src="https://github.com/user-attachments/assets/d34ea64b-2faa-4ffe-829a-5e9876dd31e2" />


**Step 3** — In General Settings, configure the app name and visibility.

<img width="975" height="408" alt="image" src="https://github.com/user-attachments/assets/0c48a0c3-445b-47d2-b54f-71adf0b07caa" />


**Step 4** — On the **Sign-On** tab, select **Secure Web Authentication (SWA)**.

<img width="975" height="507" alt="image" src="https://github.com/user-attachments/assets/671490d8-7cf2-45e5-8397-f3625700199f" />


**Step 5** — Enter the Microsoft Azure login URL and configure the login fields.

<img width="975" height="495" alt="image" src="https://github.com/user-attachments/assets/9ced4b03-0338-49ee-a2af-367369b6a7a4" />

**Step 6** — Set the **Credential Strategy** — choose whether users set their own password or admin assigns it.

![Step 6](images/image62.png)

**Step 7** — Go to the **Assignments** tab and assign the app to users.

<img width="975" height="495" alt="image" src="https://github.com/user-attachments/assets/f5c609e3-2eec-42cd-8505-aee78c751728" />


**Step 8** — Assigned users will be prompted to save their Azure credentials the first time they click the app from their Okta dashboard.

<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/1cc9a6c8-10cf-4150-b5d6-d60d51c39bdd" />

<img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/c60df06d-2644-449a-bfa5-559908abc52c" />

<img width="975" height="561" alt="image" src="https://github.com/user-attachments/assets/6f3333c6-0a7f-4cb3-8e21-9bc94ff98e19" />

---

## 5. Integrating Active Directory with Okta

**Type:** On-Premises Active Directory (AD) → Okta Cloud Sync  
**Tool:** Okta AD Agent

This integration allows your on-premises Windows Active Directory users to log in to Okta using their existing AD credentials.

### Prerequisites
- A Windows Server with Active Directory
- Admin access to the Okta Admin Console
- Network connectivity between the AD server and Okta

### Steps

**Step 1** — In Okta Admin Console, go to **Directory → Directory Integrations** and click **Add Directory**.

<img width="975" height="525" alt="image" src="https://github.com/user-attachments/assets/ce273a74-eec6-4b77-88d1-36b45c50b11c" />

**Step 2** — Select **Active Directory** as the directory type.

<img width="975" height="528" alt="image" src="https://github.com/user-attachments/assets/6ec1e153-e468-47c9-94d4-81f3c90b27f8" />


**Step 3** — Download the **Okta AD Agent** installer from the link shown on screen.

<img width="975" height="516" alt="image" src="https://github.com/user-attachments/assets/6de54912-f10b-41f2-81a4-bf93215300df" />


**Step 4** — Run the AD Agent installer on your **Windows Server** that has Active Directory.

<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/bd87122a-7744-40ef-8cf8-0d4722b12fd1" />


**Step 5** — During installation, sign in with your **Okta Admin credentials** to link the agent to your Okta org.

<img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/77386e12-36f0-4d6c-bd85-975530172ca6" />

<img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/1074cfdb-5983-4b01-bb84-be364c1350c8" />


**Step 6** — Select the **Active Directory domain** to integrate.

<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/d5856b8c-05a1-427c-85b3-d044303b0c85" />


**Step 7** — Grant the Okta AD Agent the required **service account permissions** in AD.

<img width="975" height="525" alt="image" src="https://github.com/user-attachments/assets/f67ed248-5ad2-4d9b-98d5-0fd526611454" />


**Step 8** — The agent connects and shows **Active** status in the Okta Admin Console.

<img width="975" height="529" alt="image" src="https://github.com/user-attachments/assets/7805a58b-5347-41d7-aaf3-3467ac39f323" />


**Step 9** — Configure which **OUs (Organizational Units)** to import users from.

<img width="975" height="528" alt="image" src="https://github.com/user-attachments/assets/b1c19889-3193-4d5e-aeeb-fbbfdcae1d3d" />


**Step 10** — Run an **Import** to pull AD users into Okta.

<img width="975" height="530" alt="image" src="https://github.com/user-attachments/assets/4fd0ee77-3766-4bb9-aa10-ef485937a987" />


**Step 11** — Review imported users and confirm or auto-confirm the matches.

<img width="975" height="528" alt="image" src="https://github.com/user-attachments/assets/39970c81-43d7-4edd-b53a-7306c25d16ea" />


**Step 12** — Configure **attribute mappings** between AD fields and Okta profile attributes.

<img width="975" height="526" alt="image" src="https://github.com/user-attachments/assets/adf9944c-e2de-42a7-b99c-72c7992ec71f" />


**Step 13** — Active Directory integration is now complete ✅

<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/890c52ff-24b5-4a52-9cb8-37d05fd70290" />

<img width="975" height="508" alt="image" src="https://github.com/user-attachments/assets/7ceec2f4-f57c-4003-a78d-470acf1c0488" />

<img width="975" height="507" alt="image" src="https://github.com/user-attachments/assets/da324f25-aaf1-4096-8a76-8f785254afc5" />

<img width="975" height="509" alt="image" src="https://github.com/user-attachments/assets/5cb3e179-8da3-4f29-9498-19e57ec78292" />

