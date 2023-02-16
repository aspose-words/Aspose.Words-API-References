---
title: SdtListItem
second_title: Aspose.Words for C++ API Reference
description: This element specifies a single list item within a parent ComboBox or DropDownList structured document tag. To learn more, visit the  documentation article.
type: docs
weight: 92
url: /cpp/aspose.words.markup/sdtlistitem/
---
## SdtListItem class


This element specifies a single list item within a parent [ComboBox](../sdttype/) or [DropDownList](../sdttype/) structured document tag. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class SdtListItem : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayText](./get_displaytext/)() const | Gets the text to display in the run content in place of the [Value](./get_value/) attribute contents for this list item. |
| [get_Value](./get_value/)() const | Gets the value of this list item. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SdtListItem](./sdtlistitem/)(const System::String\&, const System::String\&) | Initializes a new instance of this class. |
| [SdtListItem](./sdtlistitem/)(const System::String\&) | Initializes a new instance of this class. |
| static [Type](./type/)() |  |

## Examples



Shows how to work with drop down-list structured document tags. 
```cpp
auto doc = MakeObject<Document>();
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::DropDownList, MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild(tag);

// A drop-down list structured document tag is a form that allows the user to
// select an option from a list by left-clicking and opening the form in Microsoft Word.
// The "ListItems" property contains all list items, and each list item is an "SdtListItem".
SharedPtr<SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(MakeObject<SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Add 3 more list items. Initialize these items using a different constructor to the first item
// to display strings that are different from their values.
listItems->Add(MakeObject<SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(MakeObject<SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(MakeObject<SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// The drop-down list is displaying the first item. Assign a different list item to the "SelectedValue" to display it.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Enumerate over the collection and print each element.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << "List item: " << enumerator->get_Current()->get_DisplayText() << ", value: " << enumerator->get_Current()->get_Value()
                      << std::endl;
        }
    }
}

// Remove the last list item.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(ArtifactsDir + u"StructuredDocumentTag.ListItemCollection.docx");

// Use the "Clear" method to empty the entire drop-down item collection at once.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words](../../)
