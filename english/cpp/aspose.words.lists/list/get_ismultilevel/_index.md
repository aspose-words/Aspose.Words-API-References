---
title: Aspose::Words::Lists::List::get_IsMultiLevel method
linktitle: get_IsMultiLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::List::get_IsMultiLevel method. Returns true when the list contains 9 levels; false when 1 level in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.lists/list/get_ismultilevel/
---
## List::get_IsMultiLevel method


Returns **true** when the list contains 9 levels; **false** when 1 level.

```cpp
bool Aspose::Words::Lists::List::get_IsMultiLevel()
```

## Remarks


The lists that you create with Aspose.Words are always multi-level lists and contain 9 levels.

Microsoft Word 2003 and later always create multi-level lists with 9 levels. But in some documents, created with earlier versions of Microsoft Word you might encounter lists that have 1 level only.

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

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
