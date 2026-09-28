---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/compliance/
---

## PdfSaveOptions.compliance property

Specifies the PDF standards compliance level for output documents.


```python
@property
def compliance(self) -> aspose.words.saving.PdfCompliance:
    ...

@compliance.setter
def compliance(self, value: aspose.words.saving.PdfCompliance):
    ...

```

### Remarks

Default is [PdfCompliance.PDF17](../../pdfcompliance/#PDF17).




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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

