---
title: PdfEncryptionDetails.Permissions
linktitle: Permissions
articleTitle: Permissions
second_title: 用于 .NET 的 Aspose.Words
description: PdfEncryptionDetails Permissions 财产. 指定允许用户对加密的 PDF 文档进行的操作 默认值为DisallowAll 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

指定允许用户对加密的 PDF 文档进行的操作。 默认值为DisallowAll.

```csharp
public PdfPermissions Permissions { get; set; }
```

## 例子

展示如何对已保存的 PDF 文档设置权限。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// 首先禁止所有权限。
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// 扩展权限以允许编辑注释。
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 通过“EncryptionDetails”属性启用加密。
saveOptions.EncryptionDetails = encryptionDetails;

// 当我们打开这个文档时，我们需要在访问它的内容之前提供密码。
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### 也可以看看

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
