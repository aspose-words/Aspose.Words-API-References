---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart class
linktitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart class. Represents a start of ranged structured document tag which accepts multi-sections content. See also StructuredDocumentTagRangeEnd. To learn more, visit the Structured Document Tags or Content Control documentation article in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Represents a start of ranged structured document tag which accepts multi-sections content. See also [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). 
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public IStructuredDocumentTag
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Adds the specified node to the end of the stdContent range. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Returns a live collection of child nodes that match the specified types. |
| [GetEnumerator](./getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [RemoveAllChildren](./removeallchildren/)() | Removes all the nodes between this range start node and the range end node. |
| [RemoveSelfOnly](./removeselfonly/)() override | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&, Aspose::Words::Markup::SdtType) | Initializes a new instance of the Structured document tag range start class. |
| static [Type](./type/)() |  |
| [get_Appearance](./get_appearance/)() override | Gets or sets the appearance of the structured document tag. |
| [get_Color](./get_color/)() override | Gets or sets the color of the structured document tag. |
| [get_Id](./get_id/)() override | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). 

 if set to **true**, this state shall be resumed (showing placeholder text) upon opening this document. |
| [get_LastChild](./get_lastchild/)() | Gets the last child in the stdContent range. |
| [get_Level](./get_level/)() const override | Gets the level at which this structured document tag range start occurs in the document tree. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | When set to **true**, this property will prohibit a user from deleting this structured document tag. |
| [get_LockContents](./get_lockcontents/)() override | When set to **true**, this property will prohibit a user from editing the contents of this structured document tag. |
| [get_NodeType](./get_nodetype/)() const override | Returns [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_Placeholder](./get_placeholder/)() override | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [XmlMapping](./get_xmlmapping/) element or the [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) element is **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [get_RangeEnd](./get_rangeend/)() | Specifies end of range if the [StructuredDocumentTag](../structureddocumenttag/) is a ranged structured document tag. Otherwise returns **null**. |
| [get_SdtType](./get_sdttype/)() override | Gets type of this structured document tag. |
| [get_Tag](./get_tag/)() const override | Specifies a tag associated with the current structured document tag node. Can not be **null**. |
| [get_Title](./get_title/)() const override | Specifies the friendly name associated with this structured document tag. Can not be **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. Unlike the [WordOpenXML](./get_wordopenxml/) property, this method generates a stripped-down document that excludes any non-content-related parts. |
| [get_XmlMapping](./get_xmlmapping/)() override | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Sets the appearance of the structured document tag. |
| [set_Color](./set_color/)(System::Drawing::Color) override | Sets the color of the structured document tag. |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). 

 if set to **true**, this state shall be resumed (showing placeholder text) upon opening this document. |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | When set to **true**, this property will prohibit a user from deleting this structured document tag. |
| [set_LockContents](./set_lockcontents/)(bool) override | When set to **true**, this property will prohibit a user from editing the contents of this structured document tag. |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [set_Tag](./set_tag/)(System::String) override | Specifies a tag associated with the current structured document tag node. Can not be **null**. |
| [set_Title](./set_title/)(System::String) override | Specifies the friendly name associated with this structured document tag. Can not be **null**. |
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

 Can be immediate child of [Body](../../aspose.words/body/) node only. 
## Examples


Shows how to get the properties of multi-section structured document tags.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Multi-section structured document tags.docx"));

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));


std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```
## See Also

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
