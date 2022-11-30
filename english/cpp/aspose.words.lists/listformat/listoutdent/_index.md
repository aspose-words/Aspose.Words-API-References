---
title: ListOutdent
second_title: Aspose.Words for C++ API Reference
description: Decreases the list level of the current paragraph by one level.
type: docs
weight: 92
url: /cpp/aspose.words.lists/listformat/listoutdent/
---
## ListFormat::ListOutdent method


Decreases the list level of the current paragraph by one level.

```cpp
void Aspose::Words::Lists::ListFormat::ListOutdent()
```

## Remarks


This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. [List](../../list/) formatting for each level specifies what bullet or number is used, left indent, space between the bullet and text etc.

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

## See Also

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words](../../../)
