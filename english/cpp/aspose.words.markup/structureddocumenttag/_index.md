---
title: Aspose::Words::Markup::StructuredDocumentTag class
linktitle: StructuredDocumentTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag class. Represents a structured document tag (SDT or content control) in a document. To learn more, visit the Structured Document Tags or Content Control documentation article in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Represents a structured document tag (SDT or content control) in a document. 
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class StructuredDocumentTag : public CompositeNode,
                              public IMarkupNode,
                              public Revisions::ITrackableNode,
                              public IRunAttrSource,
                              public IStructuredDocumentTag
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the StructuredDocumentTag. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the StructuredDocumentTag. |
| [Clear](./clear/)() | Clears contents of this structured document tag and displays a placeholder if it is defined. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Returns a live collection of child nodes that match the specified type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [RemoveSelfOnly](./removeselfonly/)() override | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String \&) | Sets the symbol used to represent the checked state of a check box content control. |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String \&) | Sets the symbol used to represent the unchecked state of a check box content control. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Initializes a new instance of the Structured document tag class. |
| static [Type](./type/)() |  |
| [get_Appearance](./get_appearance/)() override | Gets/sets the appearance of a structured document tag. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Specifies category of building block for this SDT node. Can not be **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Specifies type of building block for this SDT. Can not be **null**. |
| [get_CalendarType](./get_calendartype/)() | Specifies the type of calendar for this SDT. Default is [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Gets/Sets current state of the Checkbox SDT. Default value for this property is **false**. |
| [get_Color](./get_color/)() override | Gets or sets the color of the structured document tag. |
| [get_ContentsFont](./get_contentsfont/)() | Font formatting that will be applied to text entered into SDT. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | String that represents the format in which dates are displayed. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Allows to set/get the language format for the date displayed in this SDT. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Gets/sets format in which the date for a date SDT is stored when the SDT is bound to an XML node in the document's data store. Default value is [DateTime](../sdtdatestorageformat/) |
| [get_EndCharacterFont](./get_endcharacterfont/)() | Font formatting that will be applied to the last character of text entered into SDT. |
| [get_FullDate](./get_fulldate/)() | Specifies the full date and time last entered into this SDT. |
| [get_Id](./get_id/)() override | Specifies a unique read-only persistent numerical Id for this SDT. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). 

 if set to **true**, this state shall be resumed (showing placeholder text) upon opening this document. |
| [get_IsTemporary](./get_istemporary/)() const | Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified. |
| [get_Level](./get_level/)() const override | Gets the level at which this SDT occurs in the document tree. |
| [get_ListItems](./get_listitems/)() | Gets [SdtListItemCollection](../sdtlistitemcollection/) associated with this SDT. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | When set to **true**, this property will prohibit a user from deleting this SDT. |
| [get_LockContents](./get_lockcontents/)() override | When set to **true**, this property will prohibit a user from editing the contents of this SDT. |
| [get_Multiline](./get_multiline/)() | Specifies whether this SDT allows multiple lines of text. |
| [get_NodeType](./get_nodetype/)() const override | Returns [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_Placeholder](./get_placeholder/)() override | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [XmlMapping](./get_xmlmapping/) element or the [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) element is **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [get_SdtType](./get_sdttype/)() override | Gets type of this Structured document tag. |
| [get_Style](./get_style/)() | Gets or sets the Style of the structured document tag. |
| [get_StyleName](./get_stylename/)() | Gets or sets the name of the style applied to the structured document tag. |
| [get_Tag](./get_tag/)() const override | Specifies a tag associated with the current SDT node. Can not be **null**. |
| [get_Title](./get_title/)() const override | Specifies the friendly name associated with this SDT. Can not be **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. Unlike the [WordOpenXML](./get_wordopenxml/) property, this method generates a stripped-down document that excludes any non-content-related parts. |
| [get_XmlMapping](./get_xmlmapping/)() override | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Gets/sets the appearance of a structured document tag. |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String \&) | Specifies category of building block for this SDT node. Can not be **null**. |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String \&) | Specifies type of building block for this SDT. Can not be **null**. |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Specifies the type of calendar for this SDT. Default is [Default](../sdtcalendartype/) |
| [set_Checked](./set_checked/)(bool) | Gets/Sets current state of the Checkbox SDT. Default value for this property is **false**. |
| [set_Color](./set_color/)(System::Drawing::Color) override | Sets the color of the structured document tag. |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String \&) | String that represents the format in which dates are displayed. |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Allows to set/get the language format for the date displayed in this SDT. |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Gets/sets format in which the date for a date SDT is stored when the SDT is bound to an XML node in the document's data store. Default value is [DateTime](../sdtdatestorageformat/) |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Specifies the full date and time last entered into this SDT. |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). 

 if set to **true**, this state shall be resumed (showing placeholder text) upon opening this document. |
| [set_IsTemporary](./set_istemporary/)(bool) | Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified. |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | When set to **true**, this property will prohibit a user from deleting this SDT. |
| [set_LockContents](./set_lockcontents/)(bool) override | When set to **true**, this property will prohibit a user from editing the contents of this SDT. |
| [set_Multiline](./set_multiline/)(bool) | Specifies whether this SDT allows multiple lines of text. |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\> \&) | Sets the Style of the structured document tag. |
| [set_StyleName](./set_stylename/)(const System::String \&) | Sets the name of the style applied to the structured document tag. |
| [set_Tag](./set_tag/)(System::String) override | Specifies a tag associated with the current SDT node. Can not be **null**. |
| [set_Title](./set_title/)(System::String) override | Specifies the friendly name associated with this SDT. Can not be **null**. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) | Adds the specified node to the end of the list of child nodes for this node. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/compositenode/gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately before the specified reference node. |
| [Is](../../aspose.words/compositenode/is/)(const System::TypeInfo \&) const override |  |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String \&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String \&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| static [Type](../../aspose.words/compositenode/type/)() |  |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| virtual [GetText](../../aspose.words/node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/node/gettype/)() const override |  |
| [Is](../../aspose.words/node/is/)(const System::TypeInfo \&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| static [Type](../../aspose.words/node/type/)() |  |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| virtual [GetChildNodes](../istructureddocumenttag/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified types. |
| [GetType](../istructureddocumenttag/gettype/)() const override |  |
| [Is](../istructureddocumenttag/is/)(const System::TypeInfo \&) const override |  |
| virtual [RemoveSelfOnly](../istructureddocumenttag/removeselfonly/)() | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| static [Type](../istructureddocumenttag/type/)() |  |
| virtual [get_Appearance](../istructureddocumenttag/get_appearance/)() | Gets or sets the appearance of the structured document tag. |
| virtual [get_Color](../istructureddocumenttag/get_color/)() | Gets or sets the color of the structured document tag. |
| virtual [get_Id](../istructureddocumenttag/get_id/)() | Specifies a unique read-only persistent numerical Id for this SDT. |
| virtual [get_IsMultiSection](../istructureddocumenttag/get_ismultisection/)() | Returns true if this instance is a ranged (multi-section) structured document tag. |
| virtual [get_IsShowingPlaceholderText](../istructureddocumenttag/get_isshowingplaceholdertext/)() | Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). 

 if set to true, this state shall be resumed (showing placeholder text) upon opening this document. |
| virtual [get_Level](../istructureddocumenttag/get_level/)() const | Gets the level at which this SDT occurs in the document tree. |
| virtual [get_LockContentControl](../istructureddocumenttag/get_lockcontentcontrol/)() | When set to true, this property will prohibit a user from deleting this SDT. |
| virtual [get_LockContents](../istructureddocumenttag/get_lockcontents/)() | When set to true, this property will prohibit a user from editing the contents of this SDT. |
| virtual [get_Node](../istructureddocumenttag/get_node/)() | Returns Node object that implements this interface. |
| virtual [get_Placeholder](../istructureddocumenttag/get_placeholder/)() | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [XmlMapping](../istructureddocumenttag/get_xmlmapping/) element or the [IsShowingPlaceholderText](../istructureddocumenttag/get_isshowingplaceholdertext/) element is true. |
| virtual [get_PlaceholderName](../istructureddocumenttag/get_placeholdername/)() | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| virtual [get_SdtType](../istructureddocumenttag/get_sdttype/)() | Gets type of this Structured document tag. |
| virtual [get_Tag](../istructureddocumenttag/get_tag/)() const | Specifies a tag associated with the current SDT node. Can not be null. |
| virtual [get_Title](../istructureddocumenttag/get_title/)() const | Specifies the friendly name associated with this SDT. Can not be null. |
| virtual [get_WordOpenXML](../istructureddocumenttag/get_wordopenxml/)() | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. |
| virtual [get_XmlMapping](../istructureddocumenttag/get_xmlmapping/)() | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| virtual [set_Appearance](../istructureddocumenttag/set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Sets the appearance of the structured document tag. |
| virtual [set_Color](../istructureddocumenttag/set_color/)(System::Drawing::Color) | Sets the color of the structured document tag. |
| virtual [set_IsShowingPlaceholderText](../istructureddocumenttag/set_isshowingplaceholdertext/)(bool) | Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). 

 if set to true, this state shall be resumed (showing placeholder text) upon opening this document. |
| virtual [set_LockContentControl](../istructureddocumenttag/set_lockcontentcontrol/)(bool) | When set to true, this property will prohibit a user from deleting this SDT. |
| virtual [set_LockContents](../istructureddocumenttag/set_lockcontents/)(bool) | When set to true, this property will prohibit a user from editing the contents of this SDT. |
| virtual [set_PlaceholderName](../istructureddocumenttag/set_placeholdername/)(System::String) | Sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| virtual [set_Tag](../istructureddocumenttag/set_tag/)(System::String) | Specifies a tag associated with the current SDT node. Can not be null. |
| virtual [set_Title](../istructureddocumenttag/set_title/)(System::String) | Specifies the friendly name associated with this SDT. Can not be null. |
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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Reference a style in the document by name:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, SdtType::RichText, MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```
## See Also

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
