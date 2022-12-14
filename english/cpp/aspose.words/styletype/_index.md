---
title: StyleType
second_title: Aspose.Words for C++ API Reference
description: Represents type of the style.
type: docs
weight: 1548
url: /cpp/aspose.words/styletype/
---
## StyleType enum


Represents type of the style.

```cpp
enum class StyleType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Paragraph | 1 | The style is a paragraph style. |
| Character | 2 | The style is a character style. |
| Table | 3 | The style is a table style. |
| List | 4 | The style is a list style. |


## Examples



Shows how to create a list style and use it in a document. 
```cpp
auto doc = MakeObject<Document>();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// We can contain an entire List object within a style.
SharedPtr<Style> listStyle = doc->get_Styles()->Add(StyleType::List, u"MyListStyle");

SharedPtr<List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Change the appearance of all list levels in our list.
for (const auto& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Create another list from a list within a style.
SharedPtr<List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Add some list items that our list will format.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Create and apply another list based on the list style.
SharedPtr<List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(ArtifactsDir + u"Lists.CreateAndUseListStyle.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
