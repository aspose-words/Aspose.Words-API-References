---
title: Aspose::Words::Markup::SdtListItemCollection class
linktitle: SdtListItemCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SdtListItemCollection class. Provides access to SdtListItem elements of a structured document tag. To learn more, visit the  documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class


Provides access to [SdtListItem](../sdtlistitem/) elements of a structured document tag. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class SdtListItemCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Adds an item to this collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Clears all items from this collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets number of items in the collection. |
| [get_SelectedValue](./get_selectedvalue/)() | Specifies currently selected value in this list. Null value allowed, meaning that no currently selected entry is associated with this list item collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns a [SdtListItem](../sdtlistitem/) object given its zero-based index in the collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Removes a list item at the specified index. |
| [set_SelectedValue](./set_selectedvalue/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Setter for [Aspose::Words::Markup::SdtListItemCollection::get_SelectedValue](./get_selectedvalue/). |
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

## Examples



Shows how to work with drop down-list structured document tags. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// A drop-down list structured document tag is a form that allows the user to
// select an option from a list by left-clicking and opening the form in Microsoft Word.
// The "ListItems" property contains all list items, and each list item is an "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Add 3 more list items. Initialize these items using a different constructor to the first item
// to display strings that are different from their values.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Enumerate over the collection and print each element.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Remove the last list item.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// Use the "Clear" method to empty the entire drop-down item collection at once.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
