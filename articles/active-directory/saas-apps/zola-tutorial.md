---
title: 'Tutorial: Azure AD SSO integration with Zola'
description: Learn how to configure single sign-on between Azure Active Directory and Zola.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 09/27/2022
ms.author: jeedes

---

# Tutorial: Azure AD SSO integration with Zola

In this tutorial, you'll learn how to integrate Zola with Azure Active Directory (Azure AD). When you integrate Zola with Azure AD, you can:

* Control in Azure AD who has access to Zola.
* Enable your users to be automatically signed-in to Zola with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Zola single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Azure AD.
For more information, see [Azure built-in roles](../roles/permissions-reference.md).

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Zola supports **SP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add Zola from the gallery

To configure the integration of Zola into Azure AD, you need to add Zola from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Zola** in the search box.
1. Select **Zola** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. You can learn more about O365 wizards [here](/microsoft-365/admin/misc/azure-ad-setup-guides?view=o365-worldwide&preserve-view=true).

## Configure and test Azure AD SSO for Zola

Configure and test Azure AD SSO with Zola using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user at Zola.

To configure and test Azure AD SSO with Zola, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Zola SSO](#configure-zola-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Zola test user](#create-zola-test-user)** - to have a counterpart of B.Simon in Zola that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Zola** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

    ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Reply URL** textbox, type the URL: 
    `https://zola-prod.auth.eu-west-3.amazoncognito.com/saml2/idpresponse`

    b. In the **Sign-on URL** textbox, type the URL provided by Zola:
    `https://app.zola.fr?company=<MYCOMPANYID>`

    c. In the **Relay State** textbox, type the URL:
    `https://app.zola.fr/dashboard-v2`

    > [!NOTE]
	> The Sign-on URL value is not real. Update the value with the actual Sign on URL. Contact [Zola support team](mailto:tech@zola.fr) to get the value. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

    ![Screenshot shows the Certificate download link.](common/metadataxml.png "Certificate")

1. On the **Set up Zola** section, copy the appropriate URL(s) based on your requirement.

	![Screenshot shows how to copy the appropriate configuration URL.](common/copy-configuration-urls.png "Metadata")  

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

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Zola.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Zola**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Zola SSO

To configure single sign-on on **Zola** side, you need to send the downloaded **Certificate (Base64)** and appropriate copied URLs from Azure portal to [Zola support team](mailto:tech@zola.fr). They set this setting to have the SAML SSO connection set properly on both sides.

### Create Zola test user

In this section, you create a user called Britta Simon at Zola. Work with [Zola support team](mailto:tech@zola.fr) to add the users in the Zola platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

* Click on **Test this application** in Azure portal. This will redirect to Zola Sign on URL where you can initiate the login flow. 

* Go to Zola Sign on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you click the Zola tile in the My Apps, this will redirect to Zola Sign on URL. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Next steps

Once you configure Zola you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).