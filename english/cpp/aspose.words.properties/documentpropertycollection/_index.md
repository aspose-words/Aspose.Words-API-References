---
title: DocumentPropertyCollection
second_title: Aspose.Words for C++ API Reference
description: Base class for BuiltInDocumentProperties and CustomDocumentProperties collections. To learn more, visit the  documentation article.
type: docs
weight: 40
url: /cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


Base class for [BuiltInDocumentProperties](../builtindocumentproperties/) and [CustomDocumentProperties](../customdocumentproperties/) collections. To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) documentation article.

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](./clear/)() | Removes all properties from the collection. |
| [Contains](./contains/)(const System::String\&) | Returns **true** if a property with the specified name exists in the collection. |
| [get_Count](./get_count/)() | Gets number of items in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | Returns a [DocumentProperty](../documentproperty/) object by the name of the property. |
| [idx_get](./idx_get/)(int32_t) | Returns a [DocumentProperty](../documentproperty/) object by index. |
| [IndexOf](./indexof/)(const System::String\&) | Gets the index of a property by name. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Removes a property with the specified name from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes a property at the specified index. |
| static [Type](./type/)() |  |
## Remarks


The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.

## Examples



Shows how to work with a document's custom properties. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Custom document properties are key-value pairs that we can add to the document.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Print every custom property in the document.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(),
                                    enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value())
                  << std::endl;
    }
}

// Display the value of a custom property using a DOCPROPERTY field.
auto builder = MakeObject<DocumentBuilder>(doc);
auto field = System::DynamicCast<FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc->Save(ArtifactsDir + u"DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Remove by name:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Empty the entire collection at once:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## See Also

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words](../../)
