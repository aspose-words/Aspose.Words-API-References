---
title: "Aspose::Words::Saving::PdfPermissions 枚举"
linktitle: "PdfPermissions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfPermissions 枚举。指定在 C++ 中对加密 PDF 文档允许用户执行的操作。"
type: docs
weight: 80000
url: /zh/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


指定在加密 PDF 文档上允许用户执行的操作。

```cpp
enum class PdfPermissions
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| DisallowAll | 0 | 禁止对 PDF 文档的所有操作。这是默认值。 |
| AllowAll | 65535 | 允许对 PDF 文档的所有操作。 |
| ContentCopy | n/a | 复制或以其他方式从文档中提取文本和图形，使用不受 [ContentCopyForAccessibility](./) 控制的操作。 |
| ContentCopyForAccessibility | n/a | 提取文本和图形（以支持残障用户的可访问性或出于其他目的）。 |
| ModifyContents | n/a | 通过除受 [ModifyAnnotations](./)、[FillIn](./) 和 [DocumentAssembly](./) 控制的操作之外的其他操作修改文档内容。 |
| ModifyAnnotations | n/a | 添加或修改文本批注，填写交互式表单字段，并且如果同时设置了 [ModifyContents](./)，则创建或修改交互式表单字段（包括签名字段）。 |
| FillIn | n/a | 填写现有的交互式表单字段（包括签名字段），即使 [ModifyContents](./) 未设置。 |
| DocumentAssembly | n/a | 组装文档（插入、旋转或删除页面并创建文档大纲项或缩略图），即使 [ModifyContents](./) 未设置。 |
| Printing | n/a | 打印文档（可能不是最高质量水平，取决于是否也设置了 [HighResolutionPrinting](./)）。 |
| HighResolutionPrinting | n/a | 将文档打印为一种表示形式，可基于实现相关的算法生成 PDF 内容的忠实数字副本。当此标志未设置（且已设置 [Printing](./)）时，打印应限制为外观的低级表示，可能质量下降。 |

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
