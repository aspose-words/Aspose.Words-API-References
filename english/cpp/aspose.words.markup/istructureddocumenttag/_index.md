---
title: Aspose::Words::Markup::IStructuredDocumentTag interface
linktitle: IStructuredDocumentTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::IStructuredDocumentTag interface. Interface to define a common data for StructuredDocumentTag and StructuredDocumentTagRangeStart in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


Interface to define a common data for [StructuredDocumentTag](../structureddocumenttag/) and [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [get_Color](./get_color/)() | Gets the color of the structured document tag. |
| virtual [get_Id](./get_id/)() | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() |  |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). if set to true, this state shall be resumed (showing placeholder text) upon opening this document. |
| virtual [get_Level](./get_level/)() const | Gets the level at which this **SDT** occurs in the document tree. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | When set to true, this property will prohibit a user from deleting this **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| virtual [get_Node](./get_node/)() |  |
| virtual [get_Placeholder](./get_placeholder/)() | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [XmlMapping](./get_xmlmapping/) element or the [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) element is true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Gets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. BuildingBlock with this name [Name](../../aspose.words.buildingblocks/buildingblock/get_name/) has to be present in the [GlossaryDocument](../../aspose.words/document/get_glossarydocument/) otherwise [InvalidOperationException](../) will occur. |
| virtual [get_SdtType](./get_sdttype/)() | Gets type of this **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Specifies a tag associated with the current SDT node. Can not be null. |
| virtual [get_Title](./get_title/)() const | Specifies the friendly name associated with this **SDT**. Can not be null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsRanged](./isranged/)() | Returns true if this instance is a ranged structured document tag. |
| virtual [RemoveSelfOnly](./removeselfonly/)() |  |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Sets the color of the structured document tag. |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). if set to true, this state shall be resumed (showing placeholder text) upon opening this document. |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| virtual [set_LockContents](./set_lockcontents/)(bool) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. BuildingBlock with this name [Name](../../aspose.words.buildingblocks/buildingblock/get_name/) has to be present in the [GlossaryDocument](../../aspose.words/document/get_glossarydocument/) otherwise [InvalidOperationException](../) will occur. |
| virtual [set_Tag](./set_tag/)(System::String) | Specifies a tag associated with the current SDT node. Can not be null. |
| virtual [set_Title](./set_title/)(System::String) | Specifies the friendly name associated with this **SDT**. Can not be null. |
| virtual [StructuredDocumentTagNode](./structureddocumenttagnode/)() | Returns [Node](../../aspose.words/node/) object that implements this interface. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
