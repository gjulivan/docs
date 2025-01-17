---
title: "Migrate Existing Apps to Atlas UI"
url: /howto8/front-end/migrate-existing-projects-to-atlasui/
weight: 20
---

{{% alert color="info" %}}
The Atlas UI Resources module is deprecated, as is Atlas 2. If you are still using Atlas 2, Mendix recommends that you [migrate from Atlas 2 To Atlas 3](/refguide9/moving-from-atlas-2-to-3/).
{{% /alert %}}

## Introduction

Atlas UI brings a lot of features to the process of building an app. But what if you already have a Mendix app that looks great and runs smoothly? No problem! To get an existing Mendix app to work with Atlas UI, there are a couple of steps to follow. This how-to describes how to upgrade existing Mendix projects to Atlas UI.

This how-to teaches you how to do the following:

* Prepare your app for Atlas UI
* Replace the UI Framework module
* Replace existing navigation layouts
* Perform some optional actions

## Replacing the UI Framework Module

{{% alert color="warning" %}}
The Atlas UI Resources module is deprecated, as is Atlas 2. If you are still using Atlas 2, Mendix recommends that you [migrate from Atlas 2 To Atlas 3](/refguide9/moving-from-atlas-2-to-3/).
{{% /alert %}}

To get the full experience of Atlas UI, it’s necessary to import the Atlas UI Resources module. Every app includes a module called **UI_Resources** that can be found under **Project** > **App Store modules** in Studio Pro. This module contains all the layouts, page templates, and building blocks. The **UI Framework** folder in this module contains the old Mendix UI Framework content, which we will be upgrading to Atlas UI.

To replace the UI Framework, follow these steps:

1. Delete the **UI_Resources** module.
2. Download and import the [Atlas UI Resources](https://marketplace.mendix.com/link/component/104730) module from the Mendix Marketplace.
3. When the Atlas UI Resources module is downloaded from the Mendix Marketplace, it will be found in **App Store modules**:

    {{< figure src="/attachments/howto8/front-end/atlas-ui/migrate-existing-projects-to-atlasui/migrate_dm_appstore.png" class="no-border" >}}

After the import is complete, there may be some errors in the **Error** pane for navigation profiles or layouts that do not exist. Be sure to resolve all of these errors.

Once the Atlas UI Resources module is imported, all the new resources will be available in Studio Pro. When creating a new page, a new set of page templates for all devices will be available. In the **Toolbox**, a new tab will be added called **Building blocks**. You can drag building blocks from this pane onto your pages.

{{< figure src="/attachments/howto8/front-end/atlas-ui/migrate-existing-projects-to-atlasui/migrate_dm_bb_toolbox.png" alt="Image of Mendix Atlas UI" class="no-border" >}}

## Replacing Existing Navigation Layouts

The Atlas UI Resources module comes with navigation layouts, which are required in order to use the page templates. If your existing navigation layouts are in a separate module, you will have to replace all the layouts for your pages with the Atlas UI layouts in order to make use of the new page templates. It is possible to keep using your old navigation layouts, but you will not be able to access the full capabilities of Atlas UI if you choose to do so.

{{< figure src="/attachments/howto8/front-end/atlas-ui/migrate-existing-projects-to-atlasui/migrate_dm_navlayouts.png" class="no-border" >}}

## Reusing Parts of Your Old Theme (Optional)

A lot of Mendix projects have a custom theme. If this is the case for your project, your old theme can be found in the Project Explorer folder named **theme_old**. The Atlas UI framework is similar to the Mendix UI Framework, so it is possible to reuse parts of your custom variables file.

{{< figure src="/attachments/howto8/front-end/atlas-ui/migrate-existing-projects-to-atlasui/migrate_old_theme.png" alt="Image of Mendix Atlas UI" class="no-border" >}}

## Read More

* [Get Started with Atlas UI](/howto8/front-end/get-started-with-atlasui/)
* [Create Company Atlas UI Resources](/howto8/front-end/create-company-atlas-ui-resources/)
* [Create Custom Preview Images for Building Blocks and Page Templates](/howto8/front-end/create-custom-preview-images-for-building-blocks-and-page-templates/)
* [Share Company Atlas UI Resources](/howto8/front-end/share-company-atlas-ui-resources/)
* [Troubleshooting Atlas UI Changes](/refguide8/migration-atlas/)
