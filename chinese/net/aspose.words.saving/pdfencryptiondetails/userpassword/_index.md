---
title: PdfEncryptionDetails.UserPassword
second_title: Aspose.Words for .NET API 参考
description: PdfEncryptionDetails 财产. 指定打开加密 PDF 文档所需的用户密码
type: docs
weight: 40
url: /zh/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

指定打开加密 PDF 文档所需的用户密码。

```csharp
public string UserPassword { get; set; }
```

### 评论

需要用户密码才能打开加密的 PDF 文档进行查看。 中指定的权限[`Permissions`](../permissions/)将由阅读器软件强制执行。

用户密码可以是`无效的`或空字符串，在这种情况下，当 打开 PDF 文档时，用户不需要密码。用户密码不能与所有者密码相同。

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

* class [PdfEncryptionDetails](../)
* 命名空间 [Aspose.Words.Saving](../../pdfencryptiondetails/)
* 部件 [Aspose.Words](../../../)


