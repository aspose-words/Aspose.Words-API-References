---
title: CustomPartCollection
second_title: Aspose.Words for C++ API Reference
description: Represents a collection of CustomPart objects. To learn more, visit the  documentation article.
type: docs
weight: 14
url: /cpp/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class


Represents a collection of [CustomPart](../custompart/) objects. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/structured-document-tags-or-content-control/) documentation article.

```cpp
class CustomPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomPart>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\&) | Adds an item to the collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [Clone](./clone/)() | Makes a deep copy of this collection and its items. |
| [CustomPartCollection](./custompartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gets or sets an item at the specified index. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\&) | Gets or sets an item at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Removes an item at the specified index. |
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


You do not normally need to create instances of this class. You access custom parts related to the OOXML package via the [PackageCustomParts](../../aspose.words/document/get_packagecustomparts/) property.

## Examples



Shows how to access a document's arbitrary custom parts collection. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clone the second part, then add the clone to the collection.
SharedPtr<CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Enumerate over the collection and print every part.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << "Part index " << index << ":" << std::endl;
        std::cout << "\tName:\t\t\t\t" << enumerator->get_Current()->get_Name() << std::endl;
        std::cout << "\tContent type:\t\t" << enumerator->get_Current()->get_ContentType() << std::endl;
        std::cout << "\tRelationship type:\t" << enumerator->get_Current()->get_RelationshipType() << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal()
                          ? u"\tSourced from outside the document"
                          : String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length()))
                  << std::endl;
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
* Library [Aspose.Words](../../)
