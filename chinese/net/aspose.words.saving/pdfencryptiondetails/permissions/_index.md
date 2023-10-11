---
title: PdfEncryptionDetails.Permissions
second_title: Aspose.Words for .NET API 参考
description: PdfEncryptionDetails 财产. 指定允许用户对加密 PDF 文档进行的操作 默认值为DisallowAll.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

指定允许用户对加密 PDF 文档进行的操作。 默认值为DisallowAll.

```csharp
public PdfPermissions Permissions { get; set; }
```

### 例子

演示如何设置已保存 PDF 文档的权限。

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* 命名空间 [Aspose.Words.Saving](../../pdfencryptiondetails/)
* 部件 [Aspose.Words](../../../)


