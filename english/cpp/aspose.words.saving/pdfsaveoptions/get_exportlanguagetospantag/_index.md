---
title: get_ExportLanguageToSpanTag
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.
type: docs
weight: 209
url: /cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## Remarks


Default value is **false** and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is **true** "Span" tag is created for the text with non-default language and "Lang" attribute is attached to this tag.

This value is ignored when [ExportDocumentStructure](../get_exportdocumentstructure/) is **false**.

## Examples



Shows how to create a "Span" tag in the document structure to export the text language. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hola mundo!");

auto saveOptions = MakeObject<PdfSaveOptions>();
saveOptions->set_ExportDocumentStructure(true);
saveOptions->set_ExportLanguageToSpanTag(true);

doc->Save(ArtifactsDir + u"PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
