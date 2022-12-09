---
title: get_ExportHeadersFootersMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is PerSection for HTML/MHTML and None for EPUB.
type: docs
weight: 222
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [PerSection](../../exportheadersfootersmode/) for HTML/MHTML and [None](../../exportheadersfootersmode/) for EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Remarks


It is hard to meaningfully output headers and footers to HTML because HTML is not paginated.

When this property is [PerSection](../../exportheadersfootersmode/), Aspose.Words exports only primary headers and footers at the beginning and the end of each section.

When it is [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) only first primary header and the last primary footer (including linked to previous) are exported.

You can disable export of headers and footers altogether by setting this property to [None](../../exportheadersfootersmode/).

## Examples



Shows how to omit headers/footers when saving a document to HTML. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Header and footer types.docx");

// This document contains headers and footers. We can access them via the "HeadersFooters" collection.
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderFirst)->GetText().Trim());

// Formats such as .html do not split the document into pages, so headers/footers will not function the same way
// they would when we open the document as a .docx using Microsoft Word.
// If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
// We can use a SaveOptions object to omit headers/footers while converting to html.
auto saveOptions = MakeObject<HtmlSaveOptions>(SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(ExportHeadersFootersMode::None);

doc->Save(ArtifactsDir + u"HeaderFooter.ExportMode.html", saveOptions);

// Open our saved document and verify that it does not contain the header's text
doc = MakeObject<Document>(ArtifactsDir + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## See Also

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
