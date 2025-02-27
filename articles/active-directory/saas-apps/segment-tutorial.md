---
title: 'Tutorial: Azure Active Directory single sign-on (SSO) integration with Segment | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and Segment.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 09/01/2021
ms.author: jeedes
---

# Tutorial: Azure Active Directory single sign-on (SSO) integration with Segment

In this tutorial, you'll learn how to integrate Segment with Azure Active Directory (Azure AD). When you integrate Segment with Azure AD, you can:

* Control in Azure AD who has access to Segment.
* Enable your users to be automatically signed-in to Segment with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Segment single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Segment supports **SP and IDP** initiated SSO.
* Segment supports **Just In Time** user provisioning.
* Segment supports [Automated user provisioning](segment-provisioning-tutorial.md).

## Add Segment from the gallery

To configure the integration of Segment into Azure AD, you need to add Segment from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Segment** in the search box.
1. Select **Segment** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

## Configure and test Azure AD SSO for Segment

Configure and test Azure AD SSO with Segment using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Segment.

To configure and test Azure AD SSO with Segment, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Segment SSO](#configure-segment-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Segment test user](#create-segment-test-user)** - to have a counterpart of B.Simon in Segment that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Segment** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a value using the following pattern:
    `urn:auth0:segment-prod:samlp-<CUSTOMER_VALUE>`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://segment-prod.auth0.com/login/callback?connection=<CUSTOMER_VALUE>`

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type the URL:
    `https://app.segment.com`

	> [!NOTE]
	> These values are placeholders. You need to use the actual Identifier and Reply URL. Steps for getting these values are described later in this tutorial.

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (Base64)** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Segment** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Segment.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Segment**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Segment SSO

1. In a new web browser window, sign in to your Segment company site as an administrator.

1. Click on **Settings Icon** and scroll down to **AUTHENTICATION** and click on **Connections**.

    ![Screenshot that shows the "Settings" icon selected, and "Connections" selected from the "Authentication" menu.](./media/segment-tutorial/connections.PNG)

1. Click on **Add new Connection**.

    ![Screenshot that shows the "Connections" section with the "Add new Connection" button selected.](./media/segment-tutorial/new-connections.PNG)

1. Select **SAML 2.0** as a connection to configure and click on **Select Connection** button.

    ![Screenshot that shows the "Choose a Connection" section with "S A M L 2.0" and the "Select Connection" button selected.](./media/segment-tutorial/select-connections.PNG)

1. On the following page, perform the following steps:

    ![Screenshot that shows the "Configure Identity Provider" page with the "Single Sign-On U R L" and "Audience U R L" text boxes highlighted, and the "Next" button selected.](./media/segment-tutorial/configure.PNG)

    a. Copy the **Single Sign-On URL** value and paste it into the **Reply URL** box in the **Basic SAML Configuration** dialog box in the Azure portal.

    b. Copy the ****Audience URL**** value and paste it into the **Identifier URL** box in the **Basic SAML Configuration** dialog box in the Azure portal.

    c. Click on **Next**.

    ![Segment Configuration](./media/segment-tutorial/certificate.PNG)

1. In the **SAML 2.0 Endpoint URL** box, paste the **Login URL** value that you copied from the Azure portal.

1. Open the downloaded **Cerificate(Base64)** from the Azure portal into Notepad and paste the content into the **Public Certificate** textbox.

1. Click on **Configure Connection**.

### Create Segment test user

In this section, a user called B.Simon is created in Segment. Segment supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in Segment, a new one is created after authentication.

Segment also supports automatic user provisioning, you can find more details [here](./segment-provisioning-tutorial.md) on how to configure automatic user provisioning.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to Segment Sign on URL where you can initiate the login flow.  

* Go to Segment Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the Segment for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the Segment tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Segment for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Next steps

Once you configure Segment you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
