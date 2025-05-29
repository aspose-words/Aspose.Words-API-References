---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PdfEncryptionDetails 以实现安全的 PDF 加密和可自定义的访问权限，确保您的文档受到保护。
type: docs
weight: 6250
url: /zh/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

包含 PDF 文档加密和访问权限的详细信息。

要了解更多信息，请访问[保护或加密文档](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/)文档文章。

```csharp
public class PdfEncryptionDetails
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | 初始化此类的一个实例。 |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | 初始化此类的一个实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | 指定加密 PDF 文档的所有者密码。 |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | 指定允许用户对加密 PDF 文档进行的操作。 默认值为DisallowAll. |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | 指定打开加密 PDF 文档所需的用户密码。 |

## 例子

展示如何设置已保存的 PDF 文档的权限。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// 扩展权限以允许编辑注释。
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();
// 通过“EncryptionDetails”属性启用加密。
saveOptions.EncryptionDetails = encryptionDetails;

// 当我们打开此文档时，我们需要提供密码才能访问其内容。
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
