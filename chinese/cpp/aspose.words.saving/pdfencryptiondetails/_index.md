---
title: "Aspose::Words::Saving::PdfEncryptionDetails 类"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfEncryptionDetails 类。包含对 PDF 文档进行加密和访问权限的详细信息。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


包含对 PDF 文档进行加密和访问权限的详细信息。欲了解更多，请访问 [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/) 文档文章。

```cpp
class PdfEncryptionDetails : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | 指定加密 PDF 文档的所有者密码。 |
| [get_Permissions](./get_permissions/)() const | 指定在加密 PDF 文档上允许用户执行的操作。默认值为[DisallowAll](../pdfpermissions/)。 |
| [get_UserPassword](./get_userpassword/)() const | 指定打开加密 PDF 文档所需的用户密码。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | 初始化此类的实例。 |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | 初始化此类的实例。 |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/) 的 setter。 |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | 指定在加密 PDF 文档上允许用户执行的操作。默认值为[DisallowAll](../pdfpermissions/)。 |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/) 的 setter。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
