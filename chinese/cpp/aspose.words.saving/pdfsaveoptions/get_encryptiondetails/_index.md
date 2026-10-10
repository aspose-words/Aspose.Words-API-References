---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails 方法"
linktitle: "get_EncryptionDetails"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails 方法。获取或设置用于在 C++ 中加密输出 PDF 文档的详细信息。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


获取或设置用于加密输出 PDF 文档的详细信息。

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## 备注


默认值为 **null**，输出文档将不会被加密。当此属性设置为有效的 [PdfEncryptionDetails](../../pdfencryptiondetails/) 对象时，输出 PDF 文档将被加密。

在保存为符合 PDF 1.7（包括 PDF/UA-1）的文档时使用 AES-128 加密算法。在保存为符合 PDF 2.0 的文档时使用 AES-256 加密算法。

PDF/A 合规性禁止加密。保存为 PDF/A 时此选项将被忽略。

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## 另见

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
