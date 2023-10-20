---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions EncryptionDetails 财产. 获取或设置加密输出 PDF 文档的详细信息 在 C#.
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

默认值为`无效的`并且输出文档不会被加密。 当此属性设置为有效时[`PdfEncryptionDetails`](../../pdfencryptiondetails/)object, 那么输出的 PDF 文档将被加密。

保存为基于 PDF 1.7 的合规性（包括 PDF/UA-1）时，使用 AES-128 加密算法。 保存为基于 PDF 2.0 的合规性时，使用 AES-256 加密算法。

PDF/A 合规性禁止加密。保存为 PDF/A 时将忽略此选项。

ContentCopyForAccessibility如果输出文档已加密，则需要 PDF/UA 合规性 的许可。保存为 PDF/UA 时将自动使用此权限。

ContentCopyForAccessibility PDF 2.0 格式已弃用此权限。 保存为 PDF 2.0 时将忽略此权限。

## 例子

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

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
