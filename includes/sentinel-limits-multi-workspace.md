---
title: "include file" 
description: "include file" 
services: microsoft-sentinel
author: austinmccollum
tags: azure-service-management
ms.topic: "include"
ms.date: 10/26/2022
ms.author: austinmc
ms.custom: "include file"
---

The following limit applies to multiple workspaces in Microsoft Sentinel. Limits here are applied when working with Sentinel features across more than workspace at a time.

|Description                   | Limit        |Dependency|
-------------------------|--------------------|--------------------|
| Incident view | 100 concurrently displayed workspaces | |
| Log query | 100 Sentinel workspaces | [Log Analytics](/azure/azure-monitor/logs/cross-workspace-query#cross-resource-query-limits) |
| Analytics rules | 20 Sentinel workspaces per query | |