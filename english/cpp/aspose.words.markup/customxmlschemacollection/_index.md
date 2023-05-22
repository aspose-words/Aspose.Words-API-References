---
title: Aspose::Words::Markup::CustomXmlSchemaCollection class
linktitle: CustomXmlSchemaCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::CustomXmlSchemaCollection class. A collection of strings that represent XML schemas that are associated with a custom XML part. To learn more, visit the  documentation article in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


A collection of strings that represent XML schemas that are associated with a custom XML part. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::String\&) | Adds an item to the collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [Clone](./clone/)() | Makes a deep clone of this object. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets or sets the element at the specified index. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Gets or sets the element at the specified index. |
| [IndexOf](./indexof/)(const System::String\&) | Returns the zero-based index of the specified value in the collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Removes the specified value from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes a value at the specified index. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarks


You do not create instances of this class. You access the collection of XML schemas of a custom XML part via the [Schemas](../customxmlpart/get_schemas/) property.

## Examples



Shows how to work with an XML schema collection. 
```cpp
auto doc = MakeObject<Document>();

String xmlPartId = System::Guid::NewGuid().ToString(u"B");
String xmlPartContent = u"<root><text>Hello, World!</text></root>";
SharedPtr<CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Add an XML schema association.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clone the custom XML part's XML schema association collection,
// and then add a couple of new schemas to the clone.
SharedPtr<CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumerate the schemas and print each element.
{
    SharedPtr<System::Collections::Generic::IEnumerator<String>> enumerator = schemas->GetEnumerator();
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

ASSERT_EQ(0, schemas->get_Count());
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
