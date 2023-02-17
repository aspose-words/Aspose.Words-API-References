---
title: PdfCompliance
second_title: Aspose.Words for C++ API Reference
description: Specifies the PDF standards compliance level.
type: docs
weight: 937
url: /cpp/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enum


Specifies the PDF standards compliance level.

```cpp
enum class PdfCompliance
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Pdf17 | 0 | The output file will comply with the PDF 1.7 (ISO 32000-1) standard. |
| Pdf20 | 1 | The output file will comply with the PDF 2.0 (ISO 32000-2) standard. |
| PdfA1a | 2 | The output file will comply with the PDF/A-1a (ISO 19005-1) standard. This level includes all the requirements of PDF/A-1b and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PdfA1b | 3 | The output file will comply with the PDF/A-1b (ISO 19005-1) standard. PDF/A-1b has the objective of ensuring reliable reproduction of the visual appearance of the document. |
| PdfA2a | 4 | The output file will comply with the PDF/A-2a (ISO 19005-2) standard. This level includes all the requirements of PDF/A-2u and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PdfA2u | 5 | The output file will comply with the PDF/A-2u (ISO 19005-2) standard. PDF/A-2u has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally any text contained in the document can be reliably extracted as a series of Unicode codepoints. |
| PdfA4 | 6 | The output file will comply with the PDF/A-4 (ISO 19005-4:2020) standard. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally any text contained in the document can be reliably extracted as a series of Unicode codepoints. |
| PdfUa1 | 7 | The output file will comply with the PDF/UA-1 (ISO 14289-1) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible. |


## Examples



Shows how to set the PDF standards compliance level of saved PDF documents. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();

// Set the "Compliance" property to "PdfCompliance.PdfA1b" to comply with the "PDF/A-1b" standard,
// which aims to preserve the visual appearance of the document as Aspose.Words convert it to PDF.
// Set the "Compliance" property to "PdfCompliance.Pdf17" to comply with the "1.7" standard.
// Set the "Compliance" property to "PdfCompliance.PdfA1a" to comply with the "PDF/A-1a" standard,
// which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
// This helps with making documents searchable but may significantly increase the size of already large documents.
saveOptions->set_Compliance(pdfCompliance);

doc->Save(ArtifactsDir + u"PdfSaveOptions.Compliance.pdf", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
