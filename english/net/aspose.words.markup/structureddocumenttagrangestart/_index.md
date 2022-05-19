---
title: StructuredDocumentTagRangeStart
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 3800
url: /net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Represents a start of **ranged** structured document tag which accepts multi-sections content. See also [`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend).

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Constructors

| Name | Description |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart)(DocumentBase, SdtType) | Initializes a new instance of the **Structured document tag range start** class. |

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes) { get; } | Gets all nodes between this range start node and the range end node. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color) { get; set; } | Gets or sets the color of the structured document tag. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id) { get; } | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Returns true if this node can contain other nodes. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext) { get; set; } | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild) { get; } | Gets the last child in the stdContent range. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level) { get; } | Gets the level at which this structured document tag range start occurs in the document tree. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol) { get; set; } | When set to true, this property will prohibit a user from deleting this structured document tag. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents) { get; set; } | When set to true, this property will prohibit a user from editing the contents of this structured document tag. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder) { get; } | Gets the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [`XmlMapping`](./xmlmapping) element or the [`IsShowingPlaceholderText`](./isshowingplaceholdertext) element is true. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername) { get; set; } | Gets or sets Name of the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) containing placeholder text. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend) { get; } | Specifies end of range if the StructuredDocumentTag is a ranged structured document tag. Otherwise returns null. |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype) { get; } | Gets type of this structured document tag. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag) { get; set; } | Specifies a tag associated with the current structured document tag node. Can not be null. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title) { get; set; } | Specifies the friendly name associated with this structured document tag. Can not be null. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml) { get; } | Gets a string that represents the XML contained within the node in the FlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping) { get; } | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild)(Node) | Adds the specified node to the end of the stdContent range. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Gets the first ancestor of the specified object type. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes)(NodeType, bool) | Returns a live collection of child nodes that match the specified types. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator)() | Provides support for the for each style iteration over the child nodes of this node. |
| virtual [GetText](../../aspose.words/node/gettext)() | Gets the text of this node and of all its children. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren)() | Removes all the nodes between this range start node and the range end node. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly)() | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

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
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* namespace [Aspose.Words.Markup](../../aspose.words.markup)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
