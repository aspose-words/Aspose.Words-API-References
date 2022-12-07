---
title: Add
second_title: Aspose.Words for C++ API Reference
description: Creates a new user defined style and adds it the collection.
type: docs
weight: 14
url: /cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Creates a new user defined style and adds it the collection.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| type | Aspose::Words::StyleType | A [StyleType](../../styletype/) value that specifies the type of the style to create. |
| name | const System::String\& | Case sensitive name of the style to create. |
## Remarks


You can create character, paragraph or a list style.

When creating a list style, the style is created with default numbered list formatting (1 \ a \ i).

Throws an exception if a style with this name already exists.

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


Shows how to add a [Style](../../style/) to a document's styles collection. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<StyleCollection> styles = doc->get_Styles();

// Set default parameters for new styles that we may later add to this collection.
styles->get_DefaultFont()->set_Name(u"Courier New");

// If we add a style of the "StyleType.Paragraph", the collection will apply the values of
// its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);

// Add a style, and then verify that it has the default settings.
styles->Add(StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## See Also

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
