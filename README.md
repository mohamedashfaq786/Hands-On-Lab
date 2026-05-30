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

![Step 3](images/image23.png)

**Step 4** — On the **Sign-On** tab, select **SAML 2.0**.

![Step 4](images/image24.png)

**Step 5** — Copy the **Metadata URL** from Okta — you will paste this in ServiceNow.

![Step 5](images/image25.png)

**Step 6** — Log in to your **ServiceNow** instance as an admin and navigate to **Multi-Provider SSO → Identity Providers**.

![Step 6](images/image26.png)

**Step 7** — Click **New** and choose **SAML** as the type.

![Step 7](images/image27.png)

**Step 8** — Paste the **Okta Metadata URL** and click **Import**.

![Step 8](images/image28.png)

**Step 9** — Review the auto-populated SAML settings and save.

![Step 9](images/image29.png)

**Step 10** — Enable the Identity Provider and set it as default (optional).

![Step 10](images/image30.png)

**Step 11** — Back in Okta, go to the **Assignments** tab and assign users to ServiceNow.

![Step 11](images/image31.png)

**Step 12** — Test SSO by accessing ServiceNow from the Okta dashboard.

![Step 12](images/image32.png)

**Step 13** — Confirm successful login to the ServiceNow User Dashboard.

![Step 13](images/image33.png)

**Step 14** — Configure attribute mappings if needed (e.g., email, username).

![Step 14](images/image34.png)

**Step 15** — Optionally enable **Provisioning** to auto-create ServiceNow users from Okta.

![Step 15](images/image35.png)

**Step 16** — Activate provisioning and map attributes between Okta and ServiceNow.

![Step 16](images/image36.png)

**Step 17** — Test the provisioning by pushing a user to ServiceNow.

![Step 17](images/image37.png)

**Step 18** — ServiceNow SAML integration is now complete ✅

![Step 18](images/image38.png)

---

## 3. Integrating Atlassian Cloud using SAML

**Authentication Type:** SAML  
**App:** Atlassian Cloud (Jira, Confluence)

### Steps

**Step 1** — In Okta, go to **Applications → Browse App Catalog** and search for **Atlassian Cloud**.

![Step 1](images/image39.png)

**Step 2** — Select **Atlassian Cloud** and click **Add Integration**.

![Step 2](images/image40.png)

**Step 3** — Enter your Atlassian organization details in General Settings.

![Step 3](images/image41.png)

**Step 4** — On the Sign-On tab, select **SAML 2.0** and copy the Metadata URL.

![Step 4](images/image42.png)

**Step 5** — Log in to **admin.atlassian.com** → **Security → SAML single sign-on**.

![Step 5](images/image43.png)

**Step 6** — Click **Add SAML configuration** and paste the Okta **SSO URL** and **Certificate**.

![Step 6](images/image44.png)

**Step 7** — Copy the **SP Entity ID** and **ACS URL** from Atlassian and enter them back in Okta.

![Step 7](images/image45.png)

**Step 8** — Save the SAML configuration in Atlassian Admin.

![Step 8](images/image46.png)

**Step 9** — Verify the domain in Atlassian (follow the TXT record verification process).

![Step 9](images/image47.png)

**Step 10** — Enforce SSO for your Atlassian organization.

![Step 10](images/image48.png)

**Step 11** — Back in Okta, assign users or groups to the Atlassian Cloud app.

![Step 11](images/image49.png)

**Step 12** — Test login by accessing Jira or Confluence — you should be redirected to Okta for authentication.

![Step 12](images/image50.png)

**Step 13** — Confirm the SAML assertion is working (user logs in successfully).

![Step 13](images/image51.png)

**Step 14** — Configure **User Provisioning (SCIM)** in Atlassian Admin → **User provisioning**.

![Step 14](images/image52.png)

**Step 15** — Enable SCIM and copy the **SCIM Base URL** and **API Key** from Atlassian.

![Step 15](images/image53.png)

**Step 16** — In Okta, go to the **Provisioning** tab of the Atlassian Cloud app and enter the SCIM credentials.

![Step 16](images/image54.png)

**Step 17** — Enable provisioning features and test the connection.

![Step 17](images/image55.png)

**Step 18** — Atlassian Cloud SAML + SCIM integration is now complete ✅

![Step 18](images/image56.png)

---

## 4. Integrating Microsoft Azure using SWA

**Authentication Type:** SWA (Secure Web Authentication)  
**App:** Microsoft Azure

> **What is SWA?** SWA (Secure Web Authentication) is used when an application does not support SAML. Okta securely stores and replays credentials on behalf of the user — like a password manager built into SSO.

### Steps

**Step 1** — In Okta, go to **Applications → Browse App Catalog** and search for **Microsoft Azure**.

![Step 1](images/image57.png)

**Step 2** — Select the app and click **Add Integration**.

![Step 2](images/image58.png)

**Step 3** — In General Settings, configure the app name and visibility.

![Step 3](images/image59.png)

**Step 4** — On the **Sign-On** tab, select **Secure Web Authentication (SWA)**.

![Step 4](images/image60.png)

**Step 5** — Enter the Microsoft Azure login URL and configure the login fields.

![Step 5](images/image61.png)

**Step 6** — Set the **Credential Strategy** — choose whether users set their own password or admin assigns it.

![Step 6](images/image62.png)

**Step 7** — Go to the **Assignments** tab and assign the app to users.

![Step 7](images/image63.png)

**Step 8** — Assigned users will be prompted to save their Azure credentials the first time they click the app from their Okta dashboard.

![Step 8](images/image64.png)

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

![Step 1](images/image65.png)

**Step 2** — Select **Active Directory** as the directory type.

![Step 2](images/image66.png)

**Step 3** — Download the **Okta AD Agent** installer from the link shown on screen.

![Step 3](images/image67.png)

**Step 4** — Run the AD Agent installer on your **Windows Server** that has Active Directory.

![Step 4](images/image68.png)

**Step 5** — During installation, sign in with your **Okta Admin credentials** to link the agent to your Okta org.

![Step 5](images/image69.png)

**Step 6** — Select the **Active Directory domain** to integrate.

![Step 6](images/image70.png)

**Step 7** — Grant the Okta AD Agent the required **service account permissions** in AD.

![Step 7](images/image71.png)

**Step 8** — The agent connects and shows **Active** status in the Okta Admin Console.

![Step 8](images/image72.png)

**Step 9** — Configure which **OUs (Organizational Units)** to import users from.

![Step 9](images/image73.png)

**Step 10** — Run an **Import** to pull AD users into Okta.

![Step 10](images/image74.png)

**Step 11** — Review imported users and confirm or auto-confirm the matches.

![Step 11](images/image75.png)

**Step 12** — Configure **attribute mappings** between AD fields and Okta profile attributes.

![Step 12](images/image76.png)

**Step 13** — Enable **AD-Delegated Authentication** so that users authenticate against AD passwords (not Okta passwords).

![Step 13](images/image77.png)

**Step 14** — Verify the agent status shows all agents as **Active**.

![Step 14](images/image78.png)

**Step 15** — Test login with an AD user account on the Okta login page.

![Step 15](images/image79.png)

**Step 16** — The user is authenticated against Active Directory via Okta ✅

![Step 16](images/image80.png)

**Step 17** — Active Directory integration is now complete ✅

![Step 17](images/image81.png)

---

## Summary

| # | App | Auth Type | Status |
|---|-----|-----------|--------|
| 1 | Google Workspace | SAML 2.0 | ✅ |
| 2 | ServiceNow | SAML 2.0 | ✅ |
| 3 | Atlassian Cloud | SAML 2.0 + SCIM | ✅ |
| 4 | Microsoft Azure | SWA | ✅ |
| 5 | Active Directory | AD Agent | ✅ |

---

## Key Concepts

| Term | Meaning |
|------|---------|
| **SAML** | XML-based standard for SSO — Okta sends a signed "assertion" to the app confirming the user's identity |
| **SWA** | Okta stores and replays your username/password for apps that don't support SAML |
| **IdP** | Identity Provider — Okta plays this role, handling logins |
| **SP** | Service Provider — the app (Google, Jira, etc.) that trusts Okta |
| **SCIM** | Protocol to automatically create/update/delete user accounts in apps |
| **AD Agent** | A small software installed on your Windows Server to bridge AD with Okta |

---

*Hands-on lab completed using Okta Free Developer Account.*
