---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: 用于 .NET 的 Aspose.Words
description: Watermark SetText 方法. 将文本水印添加到文档中 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

将文本水印添加到文档中。

```csharp
public void SetText(string text)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | String | 显示为水印的文本。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当文本长度超出范围或文本仅包含空格时抛出。 |
| ArgumentNullException | 当文本为空时抛出。 |

## 评论

文本长度必须在 1 到 200 的范围内。 文本不能为空或仅包含空格。

## 例子

演示如何创建文本水印。

```csharp
Document doc = new Document();

// 添加纯文本水印。
doc.Watermark.SetText("Aspose Watermark");

// 如果我们希望使用它作为水印来编辑文本格式，
// 我们可以通过在创建水印时传递一个 TextWatermarkOptions 对象来做到这一点。
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// 我们可以像这样从文档中删除水印。
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### 也可以看看

* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

将文本水印添加到文档中。

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | String | 显示为水印的文本。 |
| options | TextWatermarkOptions | 定义文本水印的附加选项。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当文本长度超出范围或文本仅包含空格时抛出。 |
| ArgumentNullException | 当文本为空时抛出。 |

## 评论

文本长度必须在 1 到 200 的范围内。 文本不能为空或仅包含空格。

如果[`TextWatermarkOptions`](../../textwatermarkoptions/)为空，水印将使用默认选项设置。

## 例子

演示如何创建文本水印。

```csharp
Document doc = new Document();

// 添加纯文本水印。
doc.Watermark.SetText("Aspose Watermark");

// 如果我们希望使用它作为水印来编辑文本格式，
// 我们可以通过在创建水印时传递一个 TextWatermarkOptions 对象来做到这一点。
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// 我们可以像这样从文档中删除水印。
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### 也可以看看

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
