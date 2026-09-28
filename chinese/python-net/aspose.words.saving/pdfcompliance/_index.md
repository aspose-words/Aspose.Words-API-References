---
title: PdfCompliance enumeration
linktitle: PdfCompliance enumeration
articleTitle: PdfCompliance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCompliance enumeration. Specifies the PDF standards compliance level."
type: docs
weight: 630
url: /zh/python-net/aspose.words.saving/pdfcompliance/
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
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
# 请注意，某些 PdfSaveOptions 在保存为某些标准时被禁止，并会自动修复。
# 使用 IWarningCallback 了解哪些选项被自动修复。
save_options = aw.saving.PdfSaveOptions()
# "Compliance" 属性设置为 "PdfCompliance.PdfA1b" 以符合 "PDF/A-1b" 标准，
# 其目的是在 Aspose.Words 将文档转换为 PDF 时保留文档的视觉外观。
# "Compliance" 属性设置为 "PdfCompliance.Pdf17" 以符合 "1.7" 标准。
# 将 "Compliance" 属性设置为 "PdfCompliance.PdfA1a" 以符合 "PDF/A-1a" 标准,
# 它同时符合 "PDF/A-1b"，并保留原始文档的结构。
# 将 "Compliance" 属性设置为 "PdfCompliance.PdfUa1" 以符合 "PDF/UA-1" (ISO 14289-1) 标准,
# 其旨在定义 PDF 中的电子文档，使文件可访问。
# 将 "Compliance" 属性设置为 "PdfCompliance.Pdf20" 以符合 "PDF 2.0" (ISO 32000-2) 标准。
# 将 "Compliance" 属性设置为 "PdfCompliance.PdfA4" 以符合 "PDF/A-4" (ISO 19004:2020) 标准,
# 它在时间上保持文档的静态视觉外观。
# 将 "Compliance" 属性设置为 "PdfCompliance.PdfA4Ua2" 以同时符合 PDF/A-4 (ISO 19005-4:2020)
# 以及 PDF/UA-2 (ISO 14289-2:2024) 标准。
# 将 "Compliance" 属性设置为 "PdfCompliance.PdfUa2" 以符合 PDF/UA-2 (ISO 14289-2:2024) 标准。
# 这有助于使文档可搜索，但可能显著增加已经很大的文档的大小。
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

