---
title: StructuredDocumentTag.DateDisplayLocale
linktitle: DateDisplayLocale
articleTitle: DateDisplayLocale
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag DateDisplayLocale 财产. 允许设置/获取在此显示的日期的语言格式特殊测试 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.markup/structureddocumenttag/datedisplaylocale/
---
## StructuredDocumentTag.DateDisplayLocale property

允许设置/获取在此显示的日期的语言格式**特殊测试**.

```csharp
public int DateDisplayLocale { get; set; }
```

## 评论

访问该属性仅适用于DateSDT 类型.

对于所有其他 SDT 类型，都会发生异常。

## 例子

演示如何提示用户输入带有结构化文档标记的日期。

```csharp
Document doc = new Document();

// 插入一个结构化文档标签，提示用户输入日期。
// 在 Microsoft Word 中，此元素称为“日期选择器内容控件”。
// 当我们在 Microsoft Word 中单击此标签右端的箭头时，
// 我们将看到一个可点击日历形式的弹出窗口。
// 我们可以使用该弹出窗口来选择标签将显示的日期。
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// 根据沙特阿拉伯阿拉伯语语言环境显示日期。
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// 设置显示日期的格式。
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// 根据回历显示日期。
sdtDate.CalendarType = SdtCalendarType.Hijri;

// 用户在 Microsoft Word 中选择日期之前，标记将显示文本“单击此处输入日期。”。
// 根据标签的日历，设置“FullDate”属性，让标签显示默认日期。
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
