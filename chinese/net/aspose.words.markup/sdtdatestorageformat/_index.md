---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Markup.SdtDateStorageFormat 如何增强 SDT 中的日期处理，确保文档中的 XML 数据无缝集成。
type: docs
weight: 4700
url: /zh/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

指定当 SDT 绑定到文档数据存储中的 XML 节点时，如何存储/检索日期 SDT 的日期。

```csharp
public enum SdtDateStorageFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Date | `0` | 日期 SDT 的日期值以标准 XML 模式日期格式存储为日期。 |
| DateTime | `1` | 日期 SDT 的日期值以标准 XML Schema DateTime 格式存储为日期。 |
| Text | `2` | 日期 SDT 的日期值存储为文本。 |
| Default | `1` | 默认为DateTime |

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

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
