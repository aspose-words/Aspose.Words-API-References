---
title: Aspose::Words::Saving::PdfTextCompression enum
linktitle: PdfTextCompression
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfTextCompression enum. Specifies a type of compression applied to all content in the PDF file except images in C++.'
type: docs
weight: 81000
url: /cpp/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enum


Specifies a type of compression applied to all content in the PDF file except images.

```cpp
enum class PdfTextCompression
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No compression. |
| Flate | 1 | Flate (ZIP) compression. |


## Examples



Shows how to apply text compression when saving a document to PDF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

for (int i = 0; i < 100; i++)
{
    builder->Writeln(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
                     u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
}

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
// compression to text when we save the document to PDF.
// Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
// to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
options->set_TextCompression(pdfTextCompression);

doc->Save(ArtifactsDir + u"PdfSaveOptions.TextCompression.pdf", options);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
