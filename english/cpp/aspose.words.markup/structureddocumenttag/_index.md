---
title: StructuredDocumentTag
second_title: Aspose.Words for C++ API Reference
description: Represents a structured document tag (SDT or content control) in a document. To learn more, visit the  documentation article.
type: docs
weight: 131
url: /cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Represents a structured document tag (SDT or content control) in a document. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/structured-document-tags-or-content-control/) documentation article.

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clear](./clear/)() | Clears contents of this structured document tag and displays a placeholder if it is defined. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [get_Appearance](./get_appearance/)() const | Gets/sets the appearance of a structured document tag. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Specifies category of building block for this **SDT** node. Can not be **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Specifies type of building block for this **SDT**. Can not be **null**. |
| [get_CalendarType](./get_calendartype/)() | Specifies the type of calendar for this **SDT**. Default is [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Gets/Sets current state of the Checkbox **SDT**. Default value for this property is **false**. |
| [get_ChildNodes](../../aspose.words/compositenode/get_childnodes/)() | Gets all immediate child nodes of this node. |
| [get_Color](./get_color/)() override | Gets or sets the color of the structured document tag. |
| [get_ContentsFont](./get_contentsfont/)() | [Font](../../aspose.words/font/) formatting that will be applied to text entered into **SDT**. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | String that represents the format in which dates are displayed. Can not be **null**. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Allows to set/get the language format for the date displayed in this **SDT**. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | [Font](../../aspose.words/font/) formatting that will be applied to the last character of text entered into **SDT**. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FullDate](./get_fulldate/)() | Specifies the full date and time last entered into this **SDT**. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_Id](./get_id/)() override | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). if set to **true**, this state shall be resumed (showing placeholder text) upon opening this document. |
| [get_IsTemporary](./get_istemporary/)() const | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_Level](./get_level/)() const override | Gets the level at which this **SDT** occurs in the document tree. |
| [get_ListItems](./get_listitems/)() | Gets [SdtListItemCollection](../sdtlistitemcollection/) associated with this **SDT**. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | When set to **true**, this property will prohibit a user from deleting this **SDT**. |
| [get_LockContents](./get_lockcontents/)() override | When set to **true**, this property will prohibit a user from editing the contents of this **SDT**. |
| [get_Multiline](./get_multiline/)() | Specifies whether this **SDT** allows multiple lines of text. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_Placeholder](./get_placeholder/)() override | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [XmlMapping](./get_xmlmapping/) element or the [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) element is **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) with this name [Name](../../aspose.words.buildingblocks/buildingblock/get_name/) has to be present in the [GlossaryDocument](../../aspose.words/document/get_glossarydocument/) otherwise [InvalidOperationException](../) will occur. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [get_SdtType](./get_sdttype/)() override | Gets type of this **Structured document tag**. |
| [get_Style](./get_style/)() | Gets or sets the [Style](../../aspose.words/style/) of the structured document tag. |
| [get_StyleName](./get_stylename/)() | Gets or sets the name of the style applied to the structured document tag. |
| [get_Tag](./get_tag/)() const override | Specifies a tag associated with the current SDT node. Can not be **null**. |
| [get_Title](./get_title/)() const override | Specifies the friendly name associated with this **SDT**. Can not be **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. |
| [get_XmlMapping](./get_xmlmapping/)() override | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately before the specified reference node. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the specified child node. |
| [RemoveSelfOnly](./removeselfonly/)() | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Setter for [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | Sets the symbol used to represent the checked state of a check box content control. |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | Sets the symbol used to represent the unchecked state of a check box content control. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Initializes a new instance of the **Structured document tag** class. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


Structured document tags (SDTs) allow to embed customer-defined semantics as well as its behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to manipulate the behavior and content of [StructuredDocumentTag](./). Mapping of SDT nodes to custom XML packages within a document can be performed with using the [XmlMapping](./get_xmlmapping/) property.

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Examples



Shows how to work with styles for content control elements. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
SharedPtr<Style> quoteStyle = doc->get_Styles()->idx_get(StyleIdentifier::Quote);
auto sdtPlainText = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Reference a style in the document by name:
auto sdtRichText = MakeObject<StructuredDocumentTag>(doc, SdtType::RichText, MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

SharedPtr<NodeCollection> tags = doc->GetChildNodes(NodeType::StructuredDocumentTag, true);

for (const auto& node : System::IterateOver(tags))
{
    auto sdt = System::DynamicCast<StructuredDocumentTag>(node);

    ASSERT_EQ(StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## See Also

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words](../../)
