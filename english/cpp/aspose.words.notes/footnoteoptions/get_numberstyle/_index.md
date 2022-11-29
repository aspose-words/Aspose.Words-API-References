---
title: get_NumberStyle
second_title: Aspose.Words for C++ API Reference
description: Specifies the number format for automatically numbered footnotes.
type: docs
weight: 14
url: /cpp/aspose.words.notes/footnoteoptions/get_numberstyle/
---
## FootnoteOptions::get_NumberStyle method


Specifies the number format for automatically numbered footnotes.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::FootnoteOptions::get_NumberStyle() override
```

## Remarks


Not all number styles are applicable for this property. For the list of applicable number styles see the Insert [Footnote](../../footnote/) or Endnote dialog box in Microsoft Word. If you select a number style that is not applicable, Microsoft Word will revert to a default value.

## Examples



Shows how to change the number style of footnote/endnote reference marks. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
// symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
// and endnotes display their numbers in lowercase Roman numerals.
ASSERT_EQ(NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
// This will not affect footnotes/endnotes with custom reference marks.
doc->get_FootnoteOptions()->set_NumberStyle(NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(NumberStyle::UppercaseLetter);

doc->Save(ArtifactsDir + u"InlineStory.RefMarkNumberStyle.docx");
```

## See Also

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words](../../../)
