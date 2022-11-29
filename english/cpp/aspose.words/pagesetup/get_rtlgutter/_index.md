---
title: get_RtlGutter
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.
type: docs
weight: 482
url: /cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
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

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
