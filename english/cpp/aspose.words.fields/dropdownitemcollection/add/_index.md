---
title: Add
second_title: Aspose.Words for C++ API Reference
description: Adds a string to the end of the collection.
type: docs
weight: 1
url: /cpp/aspose.words.fields/dropdownitemcollection/add/
---
## DropDownItemCollection::Add method


Adds a string to the end of the collection.

```cpp
int32_t Aspose::Words::Fields::DropDownItemCollection::Add(const System::String &value)
```


| Parameter | Type | Description |
| --- | --- | --- |
| value | const System::String\& | The string to add to the end of the collection. |

### ReturnValue

The zero-based index at which the new element is inserted.

## Examples



Shows how to insert a combo box field, and edit the elements in its item collection. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a combo box, and then verify its collection of drop-down items.
// In Microsoft Word, the user will click the combo box,
// and then choose one of the items of text in the collection to display.
ArrayPtr<String> items = MakeArray<String>({u"One", u"Two", u"Three"});
SharedPtr<FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
SharedPtr<DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

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
    SharedPtr<System::Collections::Generic::IEnumerator<String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
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

doc->Save(ArtifactsDir + u"FormFields.DropDownItemCollection.html");

// Empty the whole collection of drop-down items.
dropDownItems->Clear();
```

## See Also

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
