---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.PdfPermissions 枚举. 指定允许用户对加密的 PDF 文档执行的操作 在 C#.
type: docs
weight: 5510
url: /zh/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

指定允许用户对加密的 PDF 文档执行的操作。

```csharp
[Flags]
public enum PdfPermissions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| DisallowAll | `0` | 禁止对 PDF 文档进行所有操作。 这是默认值。 |
| AllowAll | `FFFF` | 允许对 PDF 文档进行所有操作。 |
| ContentCopy | `10` | 通过除 控制之外的操作从文档中复制或以其他方式提取文本和图形ContentCopyForAccessibility. |
| ContentCopyForAccessibility | `200` | 提取文本和图形（以支持残障用户的辅助功能或用于其他目的）。 |
| ModifyContents | `8` | 通过 控制之外的操作修改文档内容ModifyAnnotations,FillIn， 和DocumentAssembly. |
| ModifyAnnotations | `20` | 添加或修改文本注释，填写交互式表单字段，并且，如果ModifyContentsis 还可以设置、创建或修改交互式表单字段（包括签名字段）。 |
| FillIn | `100` | 填写现有的交互式表单字段（包括签名字段），即使ModifyContents 已清除。 |
| DocumentAssembly | `400` | 组合文档（插入、旋转或删除页面并创建文档大纲项目或缩略图 图像），即使ModifyContents很清楚。 |
| Printing | `4` | 打印文档（可能不是最高质量级别，取决于是否 HighResolutionPrinting也已设置). |
| HighResolutionPrinting | `804` | 将文档打印为一种表示形式，根据依赖于实现的算法，可以根据该表示形式生成 PDF 内容的忠实数字副本。当该标志被清除时（and Printing设置），打印应仅限于外观的低级表示， 可能质量下降。 |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
