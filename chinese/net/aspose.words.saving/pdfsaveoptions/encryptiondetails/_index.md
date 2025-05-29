---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions 的 EncryptionDetails 属性，轻松配置 PDF 加密设置，确保您的文档保持安全和受到保护。
type: docs
weight: 130
url: /zh/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

获取或设置加密输出 PDF 文档的详细信息。

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## 评论

默认值为`无效的`并且输出文档将不会被加密。 当此属性设置为有效[`PdfEncryptionDetails`](../../pdfencryptiondetails/)object, 那么输出的 PDF 文档将被加密。

保存为基于 PDF 1.7 合规性（包括 PDF/UA-1）时使用 AES-128 加密算法。 保存为基于 PDF 2.0 合规性时使用 AES-256 加密算法。

PDF/A 规范禁止加密。保存为 PDF/A 格式时，此选项将被忽略。

ContentCopyForAccessibility如果输出文档已加密，则 PDF/UA compliance 要求此权限。保存为 PDF/UA 时将自动使用此权限。

ContentCopyForAccessibility权限在 PDF 2.0 格式中已弃用。 保存为 PDF 2.0 时将忽略此权限。

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
