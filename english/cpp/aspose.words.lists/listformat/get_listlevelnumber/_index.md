---
title: get_ListLevelNumber
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the list level number (0 to 8) for the paragraph.
type: docs
weight: 79
url: /cpp/aspose.words.lists/listformat/get_listlevelnumber/
---
## ListFormat::get_ListLevelNumber method


Gets or sets the list level number (0 to 8) for the paragraph.

```cpp
int32_t Aspose::Words::Lists::ListFormat::get_ListLevelNumber()
```

## Remarks


In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [List](../get_list/) property is set to reference a valid list.

## Examples



Shows how to create bulleted and numbered lists. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create with a document builder.
// 1 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// End the bulleted list.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder->get_ListFormat()->ApplyNumberDefault();

// This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Call the "ListIndent" method to increase the current list level,
// which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// These are the first three list items of the second list level, which will maintain a count
// independent of the count of the first list level. According to the current list format,
// they will have symbols of "a.", "b.", and "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Call the "ListOutdent" method to return to the previous list level.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// These two paragraphs will continue the count of the first list level.
// These items will have symbols of "2.", and "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// If we increase the list level to a level that we have added items to previously,
// the nested list will be separate from the previous, and its numbering will start from the beginning.
// These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Outdent the list level again.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// End the numbered list.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(ArtifactsDir + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


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

## See Also

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words](../../../)
