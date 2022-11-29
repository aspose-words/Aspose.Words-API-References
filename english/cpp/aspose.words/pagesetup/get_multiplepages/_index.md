---
title: get_MultiplePages
second_title: Aspose.Words for C++ API Reference
description: For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.
type: docs
weight: 339
url: /cpp/aspose.words/pagesetup/get_multiplepages/
---
## PageSetup::get_MultiplePages method


For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.

```cpp
Aspose::Words::Settings::MultiplePagesType Aspose::Words::PageSetup::get_MultiplePages() const
```


## Examples



Shows how to set gutter margins. 
```cpp
auto doc = MakeObject<Document>();

// Insert text that spans several pages.
auto builder = MakeObject<DocumentBuilder>(doc);
for (int i = 0; i < 6; i++)
{
    builder->Write(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
                   u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(BreakType::PageBreak);
}

// A gutter adds whitespaces to either the left or right page margin,
// which makes up for the center folding of pages in a book encroaching on the page's layout.
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
pageSetup->set_RtlGutter(true);

// Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
// the left/right page side position of margins every page.
pageSetup->set_MultiplePages(MultiplePagesType::MirrorMargins);

doc->Save(ArtifactsDir + u"PageSetup.Gutter.docx");
```


Shows how to configure a document that can be printed as a book fold. 
```cpp
auto doc = MakeObject<Document>();

// Insert text that spans 16 pages.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder->InsertBreak(BreakType::PageBreak);
    builder->Write(String::Format(u"Booklet face #{0}", i));
}

// Configure the first section's "PageSetup" property to print the document in the form of a book fold.
// When we print this document on both sides, we can take the pages to stack them
// and fold them all down the middle at once. The contents of the document will line up into a book fold.
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(MultiplePagesType::BookFoldPrinting);

// We can only specify the number of sheets in multiples of 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(ArtifactsDir + u"PageSetup.Booklet.docx");
```

## See Also

* Enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
