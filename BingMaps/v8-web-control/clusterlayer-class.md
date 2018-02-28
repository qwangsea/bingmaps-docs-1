---
title: "ClusterLayer Class | Microsoft Docs"
ms.custom: ""
ms.date: "02/28/2018"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 219249aa-4e2e-45cf-b8fe-e4af9530369f
caps.latest.revision: 7
author: "rbrundritt"
ms.author: "richbrun"
manager: "stevelom"
---
# ClusterLayer Class
This is the main class that provides the clustering functionality.

## Constructor

> `ClusterLayer(pushpins: Pushpin[], options?: ClusterLayerOptions)`

## Methods

Name                                          | Return Type          | Description
--------------------------------------------- | -------------------- | --------------------------------
`clear()`                                     |                      | Clears all the data in the cluster layer.
`getDisplayedPushpins()`                      | [Pushpin](Pushpin%20Class.md)[]            | Gets the pushpins that are in the current map view. If clustering is disabled, all pushpins in the clustering layer are returned.
`getOptions()`                                  | [ClusterLayerOptions](../v8-web-control/clusterlayeroptions-object.md)  | Gets the current options used by the cluster layer.
`getPushpins()`                               | [Pushpin](Pushpin%20Class.md)[]            | Gets all pushpins that are in the layers.
`getClusterPushpinByGridKey(gridKey:number)`  | [ClusterPushpin](../v8-web-control/clusterpushpin-class.md) _or_ [Pushpin](Pushpin%20Class.md) | Gets the pushpin in the specified cluster grid cell which can be either a ClusterPushpin if there are multiple pushpins in a cell or a single Pushpin.
`getVisible()` | boolean | Returns a boolean indicating if the cluster layer is visible or not. 
`setOptions(options: ClusterLayerOptions)`    |                      | Sets the clustering options to use in the layer.
`setPushpins(pushpins: Pushpin[])`            |                      | Sets the array of pushpins that are used in the clustering layer.
`setVisible(visible: boolean)` |  | Sets the visibility of the cluster layer.

## Events ##


| Name   | Arguments    | Description   |
|--------|--------------|---------------|
| `click`      | [LayerMouseEventArgs](LayerMouseEventArgs%20Object.md) | Occurs when the mouse is used to click the map or when a touch end event occurs on a pushpin or cluster in the layer.               |
| `dblclick` | [LayerMouseEventArgs](LayerMouseEventArgs%20Object.md)| Occurs when the mouse is used to double click the map or when a touch end event occurs on a pushpin or cluster in the layer. |
| `mousedown`  | [LayerMouseEventArgs](LayerMouseEventArgs%20Object.md) | Occurs when the left mouse button is pressed or a touch start event occurs on a pushpin or cluster in the layer.                    |
| `mouseover`  | [LayerMouseEventArgs](LayerMouseEventArgs%20Object.md) | Occurs when the mouse cursor moves over top of the area covered by a pushpin or cluster in the layer.                               |
| `mouseout`   | [LayerMouseEventArgs](LayerMouseEventArgs%20Object.md) | Occurs when the mouse cursor moves out of the area covered by a pushpin or cluster in the layer.                                    |
| `mouseup`    | [LayerMouseEventArgs](LayerMouseEventArgs%20Object.md) | Occurs when the left mouse button is lifted up or when the touch end event occurs on a pushpin or cluster  in the layer.             |
| `rightclick` | [LayerMouseEventArgs](LayerMouseEventArgs%20Object.md) | Occurs when the right mouse button is used to click the map or when a long touch press occurs on a pushpin or cluster in the layer. |