---
# required metadata

title: Developer's Guide | Azure RMS
description: Overview of developer tools use; SDKs, additional libraries, and code examples.
keywords:
author: bruceperlerms
manager: mbaldwin
ms.date: 09/25/2016
ms.topic: article
ms.prod:
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: a22e6bd0-8ce8-45b4-9a32-273126ab831e
# optional metadata

#ROBOTS:
audience: developer
#ms.devlang:
ms.reviewer: shubhamp
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Developer's Guide

## Overview ##
This guide outlines our suite of Rights Management SDKs and a growing set of tools and code samples that span all supported platforms.

## Software Development Kits ##
Three generations of RMS SDK are now available, outlined in the following table.

| SDK | Description |
|------|---------|
| [RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) | A simplified, next-generation tool set that provides a lightweight development experience for enabling your Android, iOS, Mac OS X, Windows Phone/RT and Linux/C++ device apps with information protection via Microsoft Rights Management services |
| [RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) | A powerful SDK offering for Windows desktop application developers and server based solution providers to enable their products with rights management|
|[AD RMS SDK](https://msdn.microsoft.com/library/cc530379.aspx)|** NOTE ** - AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, and Windows Vista. It may be altered or unavailable in subsequent versions. Instead, use Microsoft Rights Management Services SDK 2.1, which leverages functionality exposed by the client in Msipc.dll.|
|[AD RMS Scripting API](https://msdn.microsoft.com/en-us/library/bb968797.aspx)| Used to create scripts to administer an AD RMS installation|

## PowerShell guidance

[Azure Rights Management Cmdlets](https://msdn.microsoft.com/library/azure/dn629398.aspx) let you administer Azure RMS from the command line. Although this enables automation, it also supports reliable and repeated processes to help reduce administrative overheads. In addition, some Azure RMS advanced configurations and operations require Azure PowerShell.

[RMS Protection Cmdlets](https://msdn.microsoft.com/library/azure/mt433195.aspx) can be used with Azure Rights Management (Azure RMS) data protection from Azure Information Protection, or with Active Directory Rights Management Services (AD RMS) and supplement other PowerShell modules for these Rights Management deployments. Use these RMS Protection cmdlets to bulk protect and unprotect files for any file type.

## Code Samples and Tools
This collection of Microsoft supplied RMS code samples and developer support tools spans all supported operating systems; Android, iOS/OS X, Windows Phone and Windows Desktop and is updated periodically to maintained compatibility with its supported SDK.

### Android

The following run on Android supported by [RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) and later versions of the 4.x SDK.

- [UI Library and Sample app](https://github.com/AzureAD/rms-sdk-ui-for-android) at GitHub, so you can get started quickly and re-use our standard UI in your apps.
- [Android usage scenarios](https://msdn.microsoft.com/en-us/library/dn758246(v=vs.85).aspx) in Java represent important development scenarios to get you accustomed to the RMS SDK. Examples include use of Microsoft Protected File format, custom protected file formats, and custom UI controls.

### iOS / OS X

The following run on iOS / OS X supported by [RMS SDK 4.2](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md) and later versions of the 4.x SDK.

- [iOS/OS X usage scenarios](https://msdn.microsoft.com/en-us/library/dn758307(v=vs.85).aspx) in Objective C  represent important development scenarios to get you accustomed to the RMS SDK. Examples include use of Microsoft Protected File format, custom protected file formats, and custom UI controls.
- [UI Library and Sample app](https://github.com/AzureAD/rms-sdk-ui-for-ios) at GitHub, so you can get started quickly and re-use our standard UI in your apps. Supported on **iOS only**.

### Windows Desktop

The following run on Windows Desktop supported by [RMS SDK 2.1](microsoft-information-protection-and-control-client-portal.md) and later versions of the 2.x SDK.

- [Read PFILE protected PDF](https://blogs.msdn.microsoft.com/rms/2015/11/09/reading-a-pfile-protected-pdf/) is a simple code example on our RMS Developer's Corner blog that uses the MSIPC File API to decrypt and open a PFILE protected PDF document.
- [IpcManagedAPI](https://github.com/Azure-Samples/Azure-Information-Protection-Samples/tree/master/IpcManagedAPI) is a .NET (C#) representation of RMS SDK 2.1 to make it easy for your managed application to be RMS-enabled.
- [IPCNotepad](https://github.com/Azure-Samples/Azure-Information-Protection-Samples/tree/master/IpcNotepad) is a sample RMS-enabled application that takes you through the basic steps that each RMS-enabled application should perform when protecting and consuming restricted content.
- [IpcDlp](https://github.com/Azure-Samples/Azure-Information-Protection-Samples/tree/master/IpcDlpApp) is a sample RMS-enabled Data Leak Protection (DLP) application that takes you through the basic steps that a DLP RMS-enabled application should perform by using File API for protecting and consuming restricted content.
- [IpcAzureApp](https://github.com/Azure-Samples/Azure-Information-Protection-Samples/tree/master/IpcAzureApp) is a sample that demonstrates how to use RMS SDK in Azure application to protect data in Azure Blob Storage.
- [RmsDocumentInspector](https://github.com/Azure-Samples/Azure-Information-Protection-Samples/tree/master/RmsDocumentInspector) is a tool can give information about any RMS protected file such as content-id or user rights.
- [RmsFileWatcher](https://github.com/Azure-Samples/Azure-Information-Protection-Samples/tree/master/RmsFileWatcher) is a sample that demonstrates how to build a Windows application that watches directories in the file system and applies RMS protection policies on every change, for example file added or file modified.

### Windows Store and Phone

- [UI Library for Windows Store](https://github.com/AzureAD/rms-sdk-ui-for-windowsstore) - A UI Library for Microsoft RMS SDK v4.1 for Windows Store Applications. This library is optional and a developer may choose to build their own UI when using Microsoft RMS SDK v4.1

- [UI Library for Windows Phone](https://github.com/AzureAD/rms-sdk-ui-for-winphone) - A UI Library for Microsoft RMS SDK v4.1 for Windows Phone Applications. This library is optional and a developer may choose to build their own UI when using Microsoft RMS SDK v4.1

- [Sample application](https://github.com/Azure-Samples/active-directory-dotnet-rms-windowsstore) - The Sample for Microsoft RMS SDK v4.1 for Windows Store Applications provides a basic document consumption example for the platform.
