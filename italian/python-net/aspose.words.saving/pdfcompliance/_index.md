---
title: PdfCompliance enumeration
linktitle: PdfCompliance enumeration
articleTitle: PdfCompliance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCompliance enumeration. Specifies the PDF standards compliance level."
type: docs
weight: 630
url: /it/python-net/aspose.words.saving/pdfcompliance/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
# Nota che alcune PdfSaveOptions sono proibite quando si salva secondo uno degli standard e vengono corrette automaticamente.
# Usa IWarningCallback per sapere quali opzioni sono corrette automaticamente.
save_options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA1b" per conformarsi allo standard "PDF/A-1b",
# che mira a preservare l'aspetto visivo del documento mentre Aspose.Words lo converte in PDF.
# Imposta la proprietà "Compliance" su "PdfCompliance.Pdf17" per conformarsi allo standard "1.7".
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA1a" per conformarsi allo standard "PDF/A-1a",
# che è conforme a "PDF/A-1b" oltre a preservare la struttura del documento originale.
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfUa1" per conformarsi allo standard "PDF/UA-1" (ISO 14289-1),
# che mira a definire la rappresentazione di documenti elettronici in PDF che consentono al file di essere accessibile.
# Imposta la proprietà "Compliance" su "PdfCompliance.Pdf20" per conformarsi allo standard "PDF 2.0" (ISO 32000-2).
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA4" per conformarsi allo standard "PDF/A-4" (ISO 19004:2020),
# che preserva l'aspetto visivo statico del documento nel tempo.
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfA4Ua2" per conformarsi sia a PDF/A-4 (ISO 19005-4:2020)
# e agli standard PDF/UA-2 (ISO 14289-2:2024).
# Imposta la proprietà "Compliance" su "PdfCompliance.PdfUa2" per conformarsi allo standard PDF/UA-2 (ISO 14289-2:2024).
# Questo aiuta a rendere i documenti ricercabili ma può aumentare significativamente le dimensioni di documenti già di grandi dimensioni.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

