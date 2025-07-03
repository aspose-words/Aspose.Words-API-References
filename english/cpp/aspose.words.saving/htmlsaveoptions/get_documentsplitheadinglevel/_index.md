---
title: Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel method
linktitle: get_DocumentSplitHeadingLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel method. Specifies the maximum level of headings at which to split the document. Default value is %2 in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Specifies the maximum level of headings at which to split the document. Default value is **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Remarks


When [DocumentSplitCriteria](../get_documentsplitcriteria/) includes [HeadingParagraph](../../documentsplitcriteria/) and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using **Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split. Setting this property to zero will cause the document not to be split at heading paragraphs at all.

## Examples



Shows how to split an output HTML document by headings into several parts. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Every paragraph that we format using a "Heading" style can serve as a heading.
// Each heading may also have a heading level, determined by the number of its heading style.
// The headings below are of levels 1-3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Create a HtmlSaveOptions object and set the split criteria to "HeadingParagraph".
// These criteria will split the document at paragraphs with "Heading" styles into several smaller documents,
// and save each document in a separate HTML file in the local file system.
// We will also set the maximum heading level, which splits the document to 2.
// Saving the document will split it at headings of levels 1 and 2, but not at 3 to 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// Our document has four headings of levels 1 - 2. One of those headings will not be
// a split point since it is at the beginning of the document.
// The saving operation will split our document at three places, into four smaller documents.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
