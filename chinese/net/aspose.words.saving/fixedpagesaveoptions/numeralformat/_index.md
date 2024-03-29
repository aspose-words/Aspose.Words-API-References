---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: 用于 .NET 的 Aspose.Words
description: FixedPageSaveOptions NumeralFormat 财产. 获取或设置NumeralFormat用于呈现数字 默认使用欧洲数字 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

获取或设置[`NumeralFormat`](../../numeralformat/)用于呈现数字。 默认使用欧洲数字。

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## 评论

如果更改此属性的值并且页面布局已构建，则 [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/)自动调用以更新任何更改。

## 例子

显示如何设置保存为 PDF 时使用的数字格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“NumeralFormat”属性设置为“NumeralFormat.ArabicIndic”
// 使用 U+0660 到 U+0669 范围内的字形作为数字。
// 将“NumeralFormat”属性设置为“NumeralFormat.Context”
// 查找区域设置以确定要使用的字形数量。
// 将“NumeralFormat”属性设置为“NumeralFormat.EasternArabicIndic”
// 使用 U+06F0 到 U+06F9 范围内的字形作为数字。
// 将“NumeralFormat”属性设置为“NumeralFormat.European”以使用欧洲数字。
// 将“NumeralFormat”属性设置为“NumeralFormat.System”以确定区域设置中的符号集。
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### 也可以看看

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
