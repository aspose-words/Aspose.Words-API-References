---
title: ClearFormatting
second_title: Aspose.Words for C++ API Reference
description: Resets to default paragraph formatting.
type: docs
weight: 1
url: /cpp/aspose.words/paragraphformat/clearformatting/
---
## ParagraphFormat.ClearFormatting method


Resets to default paragraph formatting.

```cpp
void Aspose::Words::ParagraphFormat::ClearFormatting()
```


## Examples




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

