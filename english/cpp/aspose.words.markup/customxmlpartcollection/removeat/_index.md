---
title: Aspose::Words::Markup::CustomXmlPartCollection::RemoveAt method
linktitle: RemoveAt
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::CustomXmlPartCollection::RemoveAt method. Removes an item at the specified index in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.markup/customxmlpartcollection/removeat/
---
## CustomXmlPartCollection::RemoveAt method


Removes an item at the specified index.

```cpp
void Aspose::Words::Markup::CustomXmlPartCollection::RemoveAt(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero based index. |

## Examples



Shows how to create a structured document tag with custom XML data. 
```cpp
auto doc = MakeObject<Document>();

// Construct an XML part that contains data and add it to the document's collection.
// If we enable the "Developer" tab in Microsoft Word,
// we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
String xmlPartId = System::Guid::NewGuid().ToString(u"B");
String xmlPartContent = u"<root><text>Hello world!</text></root>";
SharedPtr<CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Below are two ways to refer to XML parts.
// 1 -  By an index in the custom XML part collection:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  By GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Add an XML schema association.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clone a part, and then insert it into the collection.
SharedPtr<CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Iterate through the collection and print the contents of each part.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << "XML part index " << index << ", ID: " << enumerator->get_Current()->get_Id() << std::endl;
        std::cout << "\tContent: " << System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data()) << std::endl;
        index++;
    }
}

// Use the "RemoveAt" method to remove the cloned part by index.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
SharedPtr<CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Create a structured document tag that will display our part's contents and insert it into the document body.
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild(tag);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.CustomXml.docx");
```

## See Also

* Class [CustomXmlPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
