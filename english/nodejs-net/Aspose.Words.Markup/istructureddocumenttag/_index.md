---
title: IStructuredDocumentTag class
linktitle: IStructuredDocumentTag class
articleTitle: IStructuredDocumentTag class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.IStructuredDocumentTag class. Interface to define a common data for [StructuredDocumentTag](../structureddocumenttag/) and [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/)."
type: docs
weight: 80
url: /nodejs-net/aspose.words.markup/istructureddocumenttag/
---

## IStructuredDocumentTag class

Interface to define a common data for [StructuredDocumentTag](../structureddocumenttag/) and [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).



### Properties

| Name | Description |
| --- | --- |
| [appearance](./appearance/) | Gets or sets the appearance of the structured document tag. |
| [color](./color/) | Gets or sets the color of the structured document tag. |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [isMultiSection](./isMultiSection/) | Returns true if this instance is a ranged (multi-section) structured document tag. |
| [isShowingPlaceholderText](./isShowingPlaceholderText/) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [level](./level/) | Gets the level at which this **SDT** occurs in the document tree. |
| [lockContentControl](./lockContentControl/) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [lockContents](./lockContents/) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [node](./node/) | Returns Node object that implements this interface. |
| [placeholder](./placeholder/) | Gets the [BuildingBlock](../../aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty,  the associated mapped XML element is empty as specified via the [IStructuredDocumentTag.xmlMapping](./xmlMapping/) element or the [IStructuredDocumentTag.isShowingPlaceholderText](./isShowingPlaceholderText/) element is true. |
| [placeholderName](./placeholderName/) | Gets or sets Name of the [BuildingBlock](../../aspose.words/buildingblock/) containing placeholder text. |
| [sdtType](./sdtType/) | Gets type of this **Structured document tag**. |
| [tag](./tag/) | Specifies a tag associated with the current SDT node. Can not be null. |
| [title](./title/) | Specifies the friendly name associated with this **SDT**. Can not be null. |
| [wordOpenXML](./wordOpenXML/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../aspose.words/saveformat/#FlatOpc) format. |
| [xmlMapping](./xmlMapping/) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |

### Methods

| Name | Description |
| --- | --- |
|[ getChildNodes(nodeType, isDeep)](./getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified types. |
|[ removeSelfOnly()](./removeSelfOnly/#default) | Removes just this SDT node itself, but keeps the content of it inside the document tree. |

### See Also

* module [Aspose.Words.Markup](../)

