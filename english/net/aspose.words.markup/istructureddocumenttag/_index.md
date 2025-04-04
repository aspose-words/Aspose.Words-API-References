---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.Markup.IStructuredDocumentTag interface for efficient management of Structured Document Tags and enhance your document processing today!
type: docs
weight: 4650
url: /net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Interface to define a common data for [`StructuredDocumentTag`](../structureddocumenttag/) and [`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/).

```csharp
public interface IStructuredDocumentTag
```

## Properties

| Name | Description |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Gets or sets the appearance of the structured document tag. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Gets or sets the color of the structured document tag. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Returns true if this instance is a ranged (multi-section) structured document tag. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Gets the level at which this **SDT** occurs in the document tree. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Returns Node object that implements this interface. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Gets the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [`XmlMapping`](./xmlmapping/) element or the [`IsShowingPlaceholderText`](./isshowingplaceholdertext/) element is true. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Gets or sets Name of the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Gets type of this **Structured document tag**. |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Specifies a tag associated with the current SDT node. Can not be null. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Specifies the friendly name associated with this **SDT**. Can not be null. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Gets a string that represents the XML contained within the node in the FlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |

## Methods

| Name | Description |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returns a live collection of child nodes that match the specified types. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Removes just this SDT node itself, but keeps the content of it inside the document tree. |

## Examples

Shows how to remove structured document tag, but keeps content inside.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// This collection provides a unified interface for accessing ranged and non-ranged structured tags. 
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### See Also

* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
