---
title: StructuredDocumentTagRangeStart
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 3740
url: /net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Represents a start of **ranged** structured document tag which accepts multi-sections content. See also [`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend).

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>
```

## Constructors

| Name | Description |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart)(DocumentBase, SdtType) | Initializes a new instance of the **Structured document tag range start** class. |

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](childnodes) { get; } | Gets all nodes between this range start node and the range end node. |
| [Color](color) { get; set; } | Gets or sets the color of the structured document tag. |
| [Id](id) { get; } | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| [IsShowingPlaceholderText](isshowingplaceholdertext) { get; set; } | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [LastChild](lastchild) { get; } | Gets the last child in the stdContent range. |
| [Level](level) { get; } | Gets the level at which this structured document tag range start occurs in the document tree. |
| [LockContentControl](lockcontentcontrol) { get; set; } | When set to true, this property will prohibit a user from deleting this structured document tag. |
| [LockContents](lockcontents) { get; set; } | When set to true, this property will prohibit a user from editing the contents of this structured document tag. |
| override [NodeType](nodetype) { get; } |  |
| [Placeholder](placeholder) { get; } | Gets the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [`XmlMapping`](./xmlmapping) element or the [`IsShowingPlaceholderText`](./isshowingplaceholdertext) element is true. |
| [PlaceholderName](placeholdername) { get; set; } | Gets or sets Name of the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) containing placeholder text. |
| [RangeEnd](rangeend) { get; } | Specifies end of range if the StructuredDocumentTag is a ranged structured document tag. Otherwise returns null. |
| [SdtType](sdttype) { get; } | Gets type of this structured document tag. |
| [Tag](tag) { get; set; } | Specifies a tag associated with the current structured document tag node. Can not be null. |
| [Title](title) { get; set; } | Specifies the friendly name associated with this structured document tag. Can not be null. |
| [WordOpenXML](wordopenxml) { get; } | Gets a string that represents the XML contained within the node in the FlatOpc format. |
| [XmlMapping](xmlmapping) { get; } | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](accept)(DocumentVisitor) |  |
| [AppendChild](appendchild)(Node) | Adds the specified node to the end of the stdContent range. |
| [GetChildNodes](getchildnodes)(NodeType, bool) | Returns a live collection of child nodes that match the specified types. |
| [GetEnumerator](getenumerator)() | Provides support for the for each style iteration over the child nodes of this node. |
| [RemoveAllChildren](removeallchildren)() | Removes all the nodes between this range start node and the range end node. |
| [RemoveSelfOnly](removeselfonly)() | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |

### Remarks

Can be immediate child of [`Body`](../../aspose.words/body) node **only**.

### Examples

Shows how to get the properties of multi-section structured document tags.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### See Also

* class [Node](../../aspose.words/node)
* namespace [Aspose.Words.Markup](../../aspose.words.markup)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
