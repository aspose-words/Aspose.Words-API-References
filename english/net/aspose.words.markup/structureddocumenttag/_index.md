---
title: Class StructuredDocumentTag
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Markup.StructuredDocumentTag class. Represents a structured document tag SDT or content control in a document in C#.
type: docs
weight: 3850
url: /net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Represents a structured document tag (SDT or content control) in a document.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Constructors

| Name | Description |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(DocumentBase, SdtType, MarkupLevel) | Initializes a new instance of the **Structured document tag** class. |

## Properties

| Name | Description |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Gets/sets the appearance of a structured document tag. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Specifies category of building block for this **SDT** node. Can not be `null`. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Specifies type of building block for this **SDT**. Can not be `null`. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Specifies the type of calendar for this **SDT**. Default is Default |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Gets/Sets current state of the Checkbox **SDT**. Default value for this property is `false`. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Gets all immediate child nodes of this node. |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Gets or sets the color of the structured document tag. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Font formatting that will be applied to text entered into **SDT**. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | String that represents the format in which dates are displayed. Can not be `null`. The dates for English (U.S.) is "mm/dd/yyyy" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Allows to set/get the language format for the date displayed in this **SDT**. |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is DateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Font formatting that will be applied to the last character of text entered into **SDT**. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Specifies the full date and time last entered into this **SDT**. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Gets the level at which this **SDT** occurs in the document tree. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Gets [`SdtListItemCollection`](../sdtlistitemcollection/) associated with this **SDT**. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | When set to `true`, this property will prohibit a user from deleting this **SDT**. |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | When set to `true`, this property will prohibit a user from editing the contents of this **SDT**. |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Specifies whether this **SDT** allows multiple lines of text. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | Returns StructuredDocumentTag. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Gets the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [`XmlMapping`](./xmlmapping/) element or the [`IsShowingPlaceholderText`](./isshowingplaceholdertext/) element is `true`. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Gets or sets Name of the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Gets type of this **Structured document tag**. |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Gets or sets the Style of the structured document tag. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Gets or sets the name of the style applied to the structured document tag. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Specifies a tag associated with the current SDT node. Can not be `null`. |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Specifies the friendly name associated with this **SDT**. Can not be `null`. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Gets a string that represents the XML contained within the node in the FlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Clears contents of this structured document tag and displays a placeholder if it is defined. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserved for system use. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Removes the specified child node. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selects the first [`Node`](../../aspose.words/node/) that matches the XPath expression. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(int, string) | Sets the symbol used to represent the checked state of a check box content control. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(int, string) | Sets the symbol used to represent the unchecked state of a check box content control. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Remarks

Structured document tags (SDTs) allow to embed customer-defined semantics as well as its behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to manipulate the behavior and content of `StructuredDocumentTag`. Mapping of SDT nodes to custom XML packages within a document can be performed with using the [`XmlMapping`](./xmlmapping/) property.

`StructuredDocumentTag` can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [`Body`](../../aspose.words/body/), [`HeaderFooter`](../../aspose.words/headerfooter/), [`Comment`](../../aspose.words/comment/), [`Footnote`](../../aspose.words.notes/footnote/) or a [`Shape`](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [`Table`](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [`Row`](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [`Paragraph`](../../aspose.words/paragraph/).
* Nested inside another `StructuredDocumentTag`.

## Examples

Shows how to work with styles for content control elements.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 -  Reference a style in the document by name:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### See Also

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
