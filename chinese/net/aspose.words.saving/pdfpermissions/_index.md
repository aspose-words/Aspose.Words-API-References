---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PdfPermissions 枚举，用于控制用户对加密 PDF 的访问。增强安全性并有效管理文档操作。
type: docs
weight: 6310
url: /zh/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

指定允许用户对加密 PDF 文档进行的操作。

```csharp
[Flags]
public enum PdfPermissions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| DisallowAll | `0` | 不允许对 PDF 文档进行所有操作。 这是默认值。 |
| AllowAll | `FFFF` | 允许对 PDF 文档进行所有操作。 |
| ContentCopy | `10` | 通过除受控操作以外的操作复制或以其他方式从文档中提取文本和图形ContentCopyForAccessibility. |
| ContentCopyForAccessibility | `200` | 提取文本和图形（以支持残障用户的可访问性或用于其他目的）。 |
| ModifyContents | `8` | 通过除受 控制的操作之外的操作修改文档内容ModifyAnnotations，FillIn， 和DocumentAssembly. |
| ModifyAnnotations | `20` | 添加或修改文本注释、填写交互式表单字段，以及，如果ModifyContentsis 还可以设置、创建或修改交互式表单字段（包括签名字段）。 |
| FillIn | `100` | 填写现有的交互式表单字段（包括签名字段），即使ModifyContents 清楚。 |
| DocumentAssembly | `400` | 组装文档（插入、旋转或删除页面以及创建文档大纲项目或缩略图 图像），即使ModifyContents很清楚。 |
| Printing | `4` | 打印文档（可能不是最高质量的，取决于是否 HighResolutionPrinting也已设置）。 |
| HighResolutionPrinting | `804` | 将文档打印到可基于实现相关的算法生成 PDF 内容真实数字副本的表示形式。当此标志被清除（并且 Printing已设置），打印应限于外观的低级表示， 可能质量下降。 |

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
