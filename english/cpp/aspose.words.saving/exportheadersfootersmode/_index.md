---
title: Aspose::Words::Saving::ExportHeadersFootersMode enum
linktitle: ExportHeadersFootersMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ExportHeadersFootersMode enum. Specifies how headers and footers are exported to HTML, MHTML or EPUB in C++.'
type: docs
weight: 55000
url: /cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Specifies how headers and footers are exported to HTML, MHTML or EPUB.

```cpp
enum class ExportHeadersFootersMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Headers and footers are not exported. |
| PerSection | 1 | Primary headers and footers are exported at the beginning and the end of each section. |
| FirstSectionHeaderLastSectionFooter | 2 | Primary header of the first section is exported at the beginning of the document and primary footer is at the end. |
| FirstPageHeaderFooterPerSection | 3 | First page header and footer are exported at the beginning and the end of each section. |


## Examples



Shows how to omit headers/footers when saving a document to HTML. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// This document contains headers and footers. We can access them via the "HeadersFooters" collection.
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// Formats such as .html do not split the document into pages, so headers/footers will not function the same way
// they would when we open the document as a .docx using Microsoft Word.
// If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
// We can use a SaveOptions object to omit headers/footers while converting to html.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Open our saved document and verify that it does not contain the header's text
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
