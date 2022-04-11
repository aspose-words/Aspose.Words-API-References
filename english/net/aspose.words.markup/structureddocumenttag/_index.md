---
title: "StructuredDocumentTag"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 3760
url: /net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Represents a structured document tag (SDT or content control) in a document.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Public Members

| Name | Description |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag)(…) | Initializes a new instance of the Structured document tag class. |
| [Appearance](appearance) { get; set; } | Gets/sets the appearance of a structured document tag. |
| [BuildingBlockCategory](buildingblockcategory) { get; set; } | Specifies category of building block for this SDT node. Can not be null. |
| [BuildingBlockGallery](buildingblockgallery) { get; set; } | Specifies type of building block for this SDT. Can not be null. |
| [CalendarType](calendartype) { get; set; } | Specifies the type of calendar for this SDT. Default is Default |
| [Checked](checked) { get; set; } | Gets/Sets current state of the Checkbox SDT. Default value for this property is false. |
| [Color](color) { get; set; } | Gets or sets the color of the structured document tag. |
| [ContentsFont](contentsfont) { get; } | Font formatting that will be applied to text entered into SDT. |
| [DateDisplayFormat](datedisplayformat) { get; set; } | String that represents the format in which dates are displayed. Can not be null. The dates for English (U.S.) is "mm/dd/yyyy" |
| [DateDisplayLocale](datedisplaylocale) { get; set; } | Allows to set/get the language format for the date displayed in this SDT. |
| [DateStorageFormat](datestorageformat) { get; set; } | Gets/sets format in which the date for a date SDT is stored when the SDT is bound to an XML node in the document's data store. Default value is DateTime |
| [EndCharacterFont](endcharacterfont) { get; } | Font formatting that will be applied to the last character of text entered into SDT. |
| [FullDate](fulldate) { get; set; } | Specifies the full date and time last entered into this SDT. |
| [Id](id) { get; } | Specifies a unique read-only persistent numerical Id for this SDT. |
| [IsShowingPlaceholderText](isshowingplaceholdertext) { get; set; } | Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [IsTemporary](istemporary) { get; set; } | Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified. |
| [Level](level) { get; } | Gets the level at which this SDT occurs in the document tree. |
| [ListItems](listitems) { get; } | Gets [`SdtListItemCollection`](../sdtlistitemcollection) associated with this SDT. |
| [LockContentControl](lockcontentcontrol) { get; set; } | When set to true, this property will prohibit a user from deleting this SDT. |
| [LockContents](lockcontents) { get; set; } | When set to true, this property will prohibit a user from editing the contents of this SDT. |
| [Multiline](multiline) { get; set; } | Specifies whether this SDT allows multiple lines of text. |
| override [NodeType](nodetype) { get; } | Returns NodeType.StructuredDocumentTag. |
| [Placeholder](placeholder) { get; } | Gets the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [`XmlMapping`](./xmlmapping) element or the [`IsShowingPlaceholderText`](./isshowingplaceholdertext) element is true. |
| [PlaceholderName](placeholdername) { get; set; } | Gets or sets Name of the [`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) containing placeholder text. |
| [SdtType](sdttype) { get; } | Gets type of this Structured document tag. |
| [Style](style) { get; set; } | Gets or sets the Style of the structured document tag. |
| [StyleName](stylename) { get; set; } | Gets or sets the name of the style applied to the structured document tag. |
| [Tag](tag) { get; set; } | Specifies a tag associated with the current SDT node. Can not be null. |
| [Title](title) { get; set; } | Specifies the friendly name associated with this SDT. Can not be null. |
| [WordOpenXML](wordopenxml) { get; } | Gets a string that represents the XML contained within the node in the FlatOpc format. |
| [XmlMapping](xmlmapping) { get; } | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| override [Accept](accept)(…) | Accepts a visitor. |
| [Clear](clear)() | Clears contents of this structured document tag and displays a placeholder if it is defined. |
| [RemoveSelfOnly](removeselfonly)() | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [SetCheckedSymbol](setcheckedsymbol)(…) | Sets the symbol used to represent the checked state of a check box content control. |
| [SetUncheckedSymbol](setuncheckedsymbol)(…) | Sets the symbol used to represent the unchecked state of a check box content control. |

### Remarks

Structured document tags (SDTs) allow to embed customer-defined semantics as well as its behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to manipulate the behavior and content of [`StructuredDocumentTag`](../structureddocumenttag). Mapping of SDT nodes to custom XML packages within a document can be performed with using the [`XmlMapping`](./xmlmapping) property.

[`StructuredDocumentTag`](../structureddocumenttag) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [`Body`](../../aspose.words/body), [`HeaderFooter`](../../aspose.words/headerfooter), [`Comment`](../../aspose.words/comment), [`Footnote`](../../aspose.words.notes/footnote) or a [`Shape`](../../aspose.words.drawing/shape) node.
* Row-level - Among rows in a table, as a child of a [`Table`](../../aspose.words.tables/table) node.
* Cell-level - Among cells in a table row, as a child of a [`Row`](../../aspose.words.tables/row) node.
* Inline-level - Among inline content inside, as a child of a [`Paragraph`](../../aspose.words/paragraph).
* Nested inside another [`StructuredDocumentTag`](../structureddocumenttag).

### Examples

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

* class [CompositeNode](../../aspose.words/compositenode)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* namespace [Aspose.Words.Markup](../../aspose.words.markup)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
