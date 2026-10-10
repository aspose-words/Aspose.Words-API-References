---
title: PdfCompliance enumeration
linktitle: PdfCompliance enumeration
articleTitle: PdfCompliance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCompliance enumeration. Specifies the PDF standards compliance level."
type: docs
weight: 630
url: /de/python-net/aspose.words.saving/pdfcompliance/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
# Beachten Sie, dass einige PdfSaveOptions beim Speichern nach einem der Standards verboten und automatisch korrigiert werden.
# Verwenden Sie IWarningCallback, um zu erfahren, welche Optionen automatisch korrigiert werden.
save_options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "Compliance" auf "PdfCompliance.PdfA1b", um dem Standard "PDF/A-1b" zu entsprechen,
# der darauf abzielt, das visuelle Erscheinungsbild des Dokuments zu erhalten, wie Aspose.Words es in PDF konvertiert.
# Setzen Sie die Eigenschaft "Compliance" auf "PdfCompliance.Pdf17", um dem Standard "1.7" zu entsprechen.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfA1a", um dem "PDF/A-1a"-Standard zu entsprechen,
# die mit "PDF/A-1b" konform ist und zudem die Dokumentenstruktur des Originaldokuments bewahrt.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfUa1", um dem "PDF/UA-1" (ISO 14289-1)-Standard zu entsprechen,
# die darauf abzielt, elektronische Dokumente im PDF zu definieren, die die Zugänglichkeit der Datei ermöglichen.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.Pdf20", um dem "PDF 2.0" (ISO 32000-2)-Standard zu entsprechen.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfA4", um dem "PDF/A-4" (ISO 19004:2020)-Standard zu entsprechen,
# die die statische visuelle Erscheinung des Dokuments über die Zeit bewahrt.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfA4Ua2", um sowohl PDF/A-4 (ISO 19005-4:2020) zu entsprechen
# und PDF/UA-2 (ISO 14289-2:2024)-Standards.
# Setzen Sie die "Compliance"-Eigenschaft auf "PdfCompliance.PdfUa2", um dem PDF/UA-2 (ISO 14289-2:2024)-Standard zu entsprechen.
# Dies hilft dabei, Dokumente durchsuchbar zu machen, kann jedoch die Größe bereits großer Dokumente erheblich erhöhen.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

