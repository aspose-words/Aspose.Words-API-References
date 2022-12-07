---
title: get_List
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the list this paragraph is a member of.
type: docs
weight: 53
url: /cpp/aspose.words.lists/listformat/get_list/
---
## ListFormat::get_List method


Gets or sets the list this paragraph is a member of.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListFormat::get_List()
```

## Remarks


The list that is being assigned to this property must belong to the current document.

The list that is being assigned to this property must not be a list style definition.

Setting this property to **null** removes bullets and numbering from the paragraph and sets the list level number to zero. Setting this property to **null** is equivalent to calling [RemoveNumbers](../removenumbers/).

## Examples



Shows how to work with list levels. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals.
for (int i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(String(u"Level ") + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(ListTemplate::BulletDefault));

for (int i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(String(u"Level ") + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(ArtifactsDir + u"Lists.SpecifyListLevel.docx");
```


Shows how to nest a list inside another list. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create an outline list for the headings.
SharedPtr<List> outlineList = doc->get_Lists()->Add(ListTemplate::OutlineNumbers);
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 1");

// Create a numbered list.
SharedPtr<List> numberedList = doc->get_Lists()->Add(ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(numberedList);
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Normal);
builder->Writeln(u"Numbered list item 1.");

// Every paragraph that comprises a list will have this flag.
ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsListItem());
ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsListItem());

// Create a bulleted list.
SharedPtr<List> bulletedList = doc->get_Lists()->Add(ListTemplate::BulletDefault);
builder->get_ListFormat()->set_List(bulletedList);
builder->get_ParagraphFormat()->set_LeftIndent(72);
builder->Writeln(u"Bulleted list item 1.");
builder->Writeln(u"Bulleted list item 2.");
builder->get_ParagraphFormat()->ClearFormatting();

// Revert to the numbered list.
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Numbered list item 2.");
builder->Writeln(u"Numbered list item 3.");

// Revert to the outline list.
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 2");

builder->get_ParagraphFormat()->ClearFormatting();

builder->get_Document()->Save(ArtifactsDir + u"Lists.NestedLists.docx");
```

## See Also

* Class [List](../../list/)
* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words](../../../)
