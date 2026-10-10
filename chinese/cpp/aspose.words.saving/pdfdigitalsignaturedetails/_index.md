---
title: "Aspose::Words::Saving::PdfDigitalSignatureDetails class"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfDigitalSignatureDetails 类。包含在 C++ 中使用数字签名对 PDF 文档进行签署的详细信息。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


包含使用数字签名对 PDF 文档进行签署的详细信息。

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | 返回包含用于签署文档的证书的证书持有者对象。 |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | 获取哈希算法。 |
| [get_Location](./get_location/)() const | 获取签署位置。 |
| [get_Reason](./get_reason/)() const | 获取签署原因。 |
| [get_SignatureDate](./get_signaturedate/)() const | 获取或设置签署日期。 |
| [get_TimestampSettings](./get_timestampsettings/)() const | 获取或设置数字签名时间戳设置。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | 初始化此类的实例。 |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | 初始化此类的实例。 |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | 返回包含用于签署文档的证书的证书持有者对象。 |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | 设置哈希算法。 |
| [set_Location](./set_location/)(const System::String\&) | 设置签署位置。 |
| [set_Reason](./set_reason/)(const System::String\&) | 设置签署原因。 |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | 用于设置 [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/) 的 setter。 |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | 用于设置 [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


目前，数字签署 PDF 文档仅在 .NET 3.5 或更高版本上可用。

当使用 Aspose.Words 创建 PDF 文档时，要对其进行数字签名，请将 [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) 属性设置为有效的 [PdfDigitalSignatureDetails](./) 对象，然后在保存文档为 PDF 格式时，将 [PdfSaveOptions](../pdfsaveoptions/) 作为参数传递给 [Save()](../) 方法。

Aspose.Words 在整个 PDF 文档上创建 PKCS#7 签名，并在创建数字签名时使用 "Adobe.PPKMS" 过滤器和 "adbe.pkcs7.sha1" 子过滤器。

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
