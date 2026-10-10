---
title: PdfCompliance enumeration
linktitle: PdfCompliance enumeration
articleTitle: PdfCompliance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCompliance enumeration. Specifies the PDF standards compliance level."
type: docs
weight: 630
url: /sv/python-net/aspose.words.saving/pdfcompliance/
---

## PdfCompliance enumeration

Specifies the PDF standards compliance level.


### Members

| Name | Description |
| --- | --- |
| PDF17 | The output file will comply with the PDF 1.7 (ISO 32000-1) standard. |
| PDF20 | The output file will comply with the PDF 2.0 (ISO 32000-2) standard. |
| PDF_A1A | The output file will comply with the PDF/A-1a (ISO 19005-1) standard. This level includes all the requirements of PDF/A-1b and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PDF_A1B | The output file will comply with the PDF/A-1b (ISO 19005-1) standard. PDF/A-1b has the objective of ensuring reliable reproduction of the visual appearance of the document. |
| PDF_A2A | The output file will comply with the PDF/A-2a (ISO 19005-2) standard. This level includes all the requirements of PDF/A-2u and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PDF_A2U | The output file will comply with the PDF/A-2u (ISO 19005-2) standard. PDF/A-2u has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints. |
| PDF_A3A | The output file will comply with the PDF/A-3a (ISO 19005-3) standard. This level includes all the requirements of PDF/A-3u and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PDF_A3U | The output file will comply with the PDF/A-3u (ISO 19005-3) standard. PDF/A-3u (as well as PDF/A-2u) has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints. In addition to PDF/A-2u, PDF/A-3u allows embedding attachments to the PDF document. |
| PDF_A4 | The output file will comply with the PDF/A-4 (ISO 19005-4:2020) standard. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints. |
| PDF_A4F | The output file will comply with the PDF/A-4f (ISO 19005-4:2020) standard. This level includes all the requirements of PDF/A-4 and additionally allows embedding attachments to the PDF document. |
| PDF_A4_UA_2 | The output file will comply with both PDF/A-4 (ISO 19005-4:2020) and PDF/UA-2 (ISO 14289-2:2024) standards. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible. |
| PDF_UA1 | The output file will comply with the PDF/UA-1 (ISO 14289-1) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible. |
| PDF_UA2 | The output file will comply with the PDF/UA-2 (ISO 14289-2:2024) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible. |

### Examples

Shows how to set the PDF standards compliance level of saved PDF documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
# Observera att vissa PdfSaveOptions är förbjudna när man sparar till ett av standarderna och automatiskt korrigeras.
# Använd IWarningCallback för att veta vilka alternativ som automatiskt korrigeras.
save_options = aw.saving.PdfSaveOptions()
# Sätt egenskapen "Compliance" till "PdfCompliance.PdfA1b" för att följa standarden "PDF/A-1b",
# som syftar till att bevara dokumentets visuella utseende när Aspose.Words konverterar det till PDF.
# Sätt egenskapen "Compliance" till "PdfCompliance.Pdf17" för att följa standarden "1.7".
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA1a" för att uppfylla standarden "PDF/A-1a",
# som uppfyller "PDF/A-1b" samt bevarar dokumentstrukturen i det ursprungliga dokumentet.
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfUa1" för att uppfylla standarden "PDF/UA-1" (ISO 14289-1),
# som syftar till att definiera och representera elektroniska dokument i PDF som gör filen tillgänglig.
# Ställ in egenskapen "Compliance" till "PdfCompliance.Pdf20" för att uppfylla standarden "PDF 2.0" (ISO 32000-2).
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA4" för att uppfylla standarden "PDF/A-4" (ISO 19004:2020),
# vilket bevarar dokumentets statiska visuella utseende över tid.
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfA4Ua2" för att uppfylla både PDF/A-4 (ISO 19005-4:2020)
# och PDF/UA-2 (ISO 14289-2:2024) standarderna.
# Ställ in egenskapen "Compliance" till "PdfCompliance.PdfUa2" för att uppfylla standarden PDF/UA-2 (ISO 14289-2:2024).
# Detta hjälper till att göra dokument sökbara men kan avsevärt öka storleken på redan stora dokument.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

