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
| virtual [get_Appearance](./get_appearance/)() | Gets or sets the appearance of the structured document tag. |
| virtual [get_Color](./get_color/)() | Gets or sets the color of the structured document tag. |
| virtual [get_Id](./get_id/)() | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Returns true if this instance is a ranged (multi-section) structured document tag. |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). if set to true, this state shall be resumed (showing placeholder text) upon opening this document. |
| virtual [get_Level](./get_level/)() const | Gets the level at which this **SDT** occurs in the document tree. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | When set to true, this property will prohibit a user from deleting this **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| virtual [get_Node](./get_node/)() | Returns [Node](../../aspose.words/node/) object that implements this interface. |
| virtual [get_Placeholder](./get_placeholder/)() | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [XmlMapping](./get_xmlmapping/) element or the [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) element is true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| virtual [get_SdtType](./get_sdttype/)() | Gets type of this **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Specifies a tag associated with the current SDT node. Can not be null. |
| virtual [get_Title](./get_title/)() const | Specifies the friendly name associated with this **SDT**. Can not be null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Gets a string that represents the XML contained within the node in the [FlatOpc](../../aspose.words/saveformat/) format. |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified types. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | Setter for [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Examples



Shows how to remove structured document tag, but keeps content inside. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// This collection provides a unified interface for accessing ranged and non-ranged structured tags.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
