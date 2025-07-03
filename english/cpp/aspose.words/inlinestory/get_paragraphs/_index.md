---
title: Aspose::Words::InlineStory::get_Paragraphs method
linktitle: get_Paragraphs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::InlineStory::get_Paragraphs method. Gets a collection of paragraphs that are immediate children of the story in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words/inlinestory/get_paragraphs/
---
## InlineStory::get_Paragraphs method


Gets a collection of paragraphs that are immediate children of the story.

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::InlineStory::get_Paragraphs() override
```


## Examples



Shows how to insert and customize footnotes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add text, and reference it with a footnote. This footnote will place a small superscript reference
// mark after the text that it references and create an entry below the main body text at the bottom of the page.
// This entry will contain the footnote's reference mark and the reference text,
// which we will pass to the document builder's "InsertFootnote" method.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// If this property is set to "true", then our footnote's reference mark
// will be its index among all the section's footnotes.
// This is the first footnote, so the reference mark will be "1".
ASSERT_TRUE(footnote->get_IsAuto());

// We can move the document builder inside the footnote to edit its reference text.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// We can set a custom reference mark which the footnote will use instead of its index number.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// A bookmark with the "IsAuto" flag set to true will still show its real index
// even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```


Shows how to add a comment to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## See Also

* Class [ParagraphCollection](../../paragraphcollection/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
