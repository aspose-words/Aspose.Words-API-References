---
title: StructuredDocumentTag.DateDisplayFormat
linktitle: DateDisplayFormat
articleTitle: DateDisplayFormat
second_title: Aspose.Words for .NET
description: 探索 StructuredDocumentTag DateDisplayFormat 属性，轻松自定义日期显示格式。提升文档的清晰度和吸引力！
type: docs
weight: 90
url: /zh/net/aspose.words.markup/structureddocumenttag/datedisplayformat/
---
## StructuredDocumentTag.DateDisplayFormat property

表示日期显示格式的字符串。

```csharp
public string DateDisplayFormat { get; set; }
```

## 评论

不可能`无效的`。

英语（美国）的日期格式为“mm/dd/yyyy”

访问此属性仅适用于Date SDT 类型。

对于所有其他 SDT 类型，都会发生异常。

## 例子

展示如何使用结构化文档标签提示用户输入日期。

```csharp
Document doc = new Document();

// 插入一个结构化文档标签，提示用户输入日期。
// 在 Microsoft Word 中，此元素称为“日期选择器内容控件”。
// 当我们在 Microsoft Word 中单击此标签右端的箭头时，
// 我们将看到一个可点击日历形式的弹出窗口。
// 我们可以使用该弹出窗口来选择标签将显示的日期。
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// 根据沙特阿拉伯阿拉伯语区域设置显示日期。
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// 设置显示日期的格式。
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// 根据伊斯兰历显示日期。
sdtDate.CalendarType = SdtCalendarType.Hijri;

// 在用户在 Microsoft Word 中选择日期之前，标签将显示文本“单击此处输入日期。”。
// 根据标签的日历，设置“FullDate”属性，让标签显示一个默认日期。
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
