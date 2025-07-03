---
title: Aspose::Words::Markup::CustomPart class
linktitle: CustomPart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::CustomPart class. Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.markup/custompart/
---
## CustomPart class


Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class CustomPart : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Makes a "deep enough" copy of the object. Does not duplicate the bytes of the [Data](./get_data/) value. |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Specifies the content type of this custom part. |
| [get_Data](./get_data/)() const | Contains the data of this custom part. |
| [get_IsExternal](./get_isexternal/)() const | False if this custom part is stored inside the OOXML package. True if this custom part is an external target. |
| [get_Name](./get_name/)() const | Gets or sets this part's absolute name within the OOXML package or the target URL. |
| [get_RelationshipType](./get_relationshiptype/)() const | Gets or sets the relationship type from the parent part to this custom part. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Setter for [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Setter for [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | Setter for [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Setter for [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## Remarks


This class represents an OOXML part that is a target of an "unknown relationship". All relationships not defined within ISO/IEC 29500 are considered "unknown relationships". Unknown relationships are permitted within an Office Open XML document provided that they conform to relationship markup guidelines.

Microsoft Word preserves custom parts during open/save cycles. Some additional info can be found here [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words also roundtrips custom parts and in addition, allows to programmatically access such parts via the [CustomPart](./) and [CustomPartCollection](../custompartcollection/) objects.

Do not confuse custom parts with Custom XML Data. Use [CustomXmlPart](../customxmlpart/) if you need to access Custom XML Data.

## Examples



Shows how to access a document's arbitrary custom parts collection. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clone the second part, then add the clone to the collection.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Enumerate over the collection and print every part.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// We can remove elements from this collection individually, or all at once.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
