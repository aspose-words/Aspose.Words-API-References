---
title: IStructuredDocumentTag class
second_title: Aspose.Words for Python via .NET API Reference
description: "Interface to define a common data for [StructuredDocumentTag](../structureddocumenttag/) and [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/)."
type: docs
weight: 80
url: /python-net/aspose.words.markup/istructureddocumenttag/
---

## IStructuredDocumentTag class

Interface to define a common data for [StructuredDocumentTag](../structureddocumenttag/) and [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).



### Properties

| Name | Description |
| --- | --- |
| [color](./color/) | Gets or sets the color of the structured document tag. |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [is_showing_placeholder_text](./is_showing_placeholder_text/) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [level](./level/) | Gets the level at which this **SDT** occurs in the document tree. |
| [lock_content_control](./lock_content_control/) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [lock_contents](./lock_contents/) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [placeholder](./placeholder/) | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty,  the associated mapped XML element is empty as specified via the [IStructuredDocumentTag.xml_mapping](./xml_mapping/) element or the [IStructuredDocumentTag.is_showing_placeholder_text](./is_showing_placeholder_text/) element is true. |
| [placeholder_name](./placeholder_name/) | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [sdt_type](./sdt_type/) | Gets type of this **Structured document tag**. |
| [tag](./tag/) | Specifies a tag associated with the current SDT node. Can not be null. |
| [title](./title/) | Specifies the friendly name associated with this **SDT**. Can not be null. |
| [word_open_xml](./word_open_xml/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC) format. |
| [xml_mapping](./xml_mapping/) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |

### Methods

| Name | Description |
| --- | --- |
|[ is_ranged()](./is_ranged/#default) | Returns true if this instance is a ranged structured document tag. |
|[ structured_document_tag_node()](./structured_document_tag_node/#default) | Returns Node object that implements this interface. |

### See Also

* module [aspose.words.markup](../)

