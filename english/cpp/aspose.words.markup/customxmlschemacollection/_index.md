---
title: Aspose::Words::Markup::CustomXmlSchemaCollection class
linktitle: CustomXmlSchemaCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::CustomXmlSchemaCollection class. A collection of strings that represent XML schemas that are associated with a custom XML part. To learn more, visit the Structured Document Tags or Content Control documentation article in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


A collection of strings that represent XML schemas that are associated with a custom XML part. 
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::String \&) | Adds an item to the collection. |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [Clone](./clone/)() | Makes a deep clone of this object. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [IndexOf](./indexof/)(const System::String \&) | Returns the zero-based index of the specified value in the collection. |
| [Remove](./remove/)(const System::String \&) | Removes the specified value from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes a value at the specified index. |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [idx_get](./idx_get/)(int32_t) | Gets or sets the element at the specified index. |
| [idx_set](./idx_set/)(int32_t, const System::String \&) | Gets or sets the element at the specified index. |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) | Const iterator type. |
| [iterator](./iterator/) | Iterator type. |
| [iterator_holder_type](./iterator_holder_type/) | A collection type whose iterator types is used as iterator types in the current collection. |
| [virtualized_iterator](./virtualized_iterator/) | Virtualized type. |
| [virtualized_iterator_element](./virtualized_iterator_element/) | Virtualized element type. |
## Remarks


You do not create instances of this class. You access the collection of XML schemas of a custom XML part via the [Schemas](../customxmlpart/get_schemas/) property.
## Examples


Shows how to work with an XML schema collection.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Add an XML schema association.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clone the custom XML part's XML schema association collection,
// and then add a couple of new schemas to the clone.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(schemas->get_Count(), 3);
ASSERT_EQ(schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"), 2);

// Enumerate the schemas and print each element.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Below are three ways of removing schemas from the collection.
// 1 -  Remove a schema by index:
schemas->RemoveAt(2);

// 2 -  Remove a schema by value:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Use the "Clear" method to empty the collection at once.
schemas->Clear();

ASSERT_EQ(schemas->get_Count(), 0);
```
## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
