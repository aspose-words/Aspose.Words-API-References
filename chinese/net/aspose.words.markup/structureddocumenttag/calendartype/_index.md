---
title: StructuredDocumentTag.CalendarType
linktitle: CalendarType
articleTitle: CalendarType
second_title: Aspose.Words for .NET
description: 探索 StructuredDocumentTag CalendarType 属性，自定义您的 SDT 日历类型。使用定制的日历选项，提升您的文档质量！
type: docs
weight: 50
url: /zh/net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

指定此日历的类型**特殊和差别待遇**. 默认为Default

```csharp
public SdtCalendarType CalendarType { get; set; }
```

## 评论

访问此属性仅适用于DateSDT 类型.

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

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
