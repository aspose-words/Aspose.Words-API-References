---
title: Aspose::Words::Fields::DropDownItemCollection::RemoveAt method
linktitle: RemoveAt
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::DropDownItemCollection::RemoveAt method. Removes a value at the specified index in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.fields/dropdownitemcollection/removeat/
---
## DropDownItemCollection::RemoveAt method


Removes a value at the specified index.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::RemoveAt(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero based index. |

## Examples



Shows how to insert a combo box field, and edit the elements in its item collection. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a combo box, and then verify its collection of drop-down items.
// In Microsoft Word, the user will click the combo box,
// and then choose one of the items of text in the collection to display.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// There are two ways of adding a new item to an existing collection of drop-down box items.
// 1 -  Append an item to the end of the collection:
dropDownItems->Add(u"Four");

// 2 -  Insert an item before another item at a specified index:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Iterate over the collection and print every element.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// There are two ways of removing elements from a collection of drop-down items.
// 1 -  Remove an item with contents equal to the passed string:
dropDownItems->Remove(u"Four");

// 2 -  Remove an item at an index:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Empty the whole collection of drop-down items.
dropDownItems->Clear();
```

## See Also

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
