---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.SdtCalendarType 枚举，使用多种日历选项增强您的 Office Open XML 文档，从而提高工作流程效率。
type: docs
weight: 4690
url: /zh/net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

指定可用于指定日历的可能类型[`CalendarType`](../structureddocumenttag/calendartype/)Office Open XML 文档中的 。

```csharp
public enum SdtCalendarType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Default | `0` | 在 OOXML 中用作默认值。等于Gregorian. |
| Gregorian | `0` | 指定应使用 ISO 8601 中定义的公历。 此日历应本地化为适当的语言。 |
| GregorianArabic | `1` | 指定应使用 ISO 8601 中定义的公历。 此日历的值应以阿拉伯语表示。 |
| GregorianMeFrench | `2` | 指定应使用 ISO 8601 中定义的公历。 此日历的值应以中东法语显示。 |
| GregorianUs | `3` | 指定应使用 ISO 8601 中定义的公历。 此日历的值应以英语表示。 |
| GregorianXlitEnglish | `4` | 指定应使用 ISO 8601 中定义的公历。 此日历的值应为对应阿拉伯字符 （公历英语的阿拉伯语音译）的英文字符串表示形式。 |
| GregorianXlitFrench | `5` | 指定应使用 ISO 8601 中定义的公历。 此日历的值应为法语字符串在阿拉伯字符中的对应表示形式 （公历的法语阿拉伯音译）。 |
| Hebrew | `6` | 指定应使用高斯公式描述的逾越节 [CITATION] 和《口传律法完全重述》（Mishneh Torah）的希伯来阴历。 |
| Hijri | `7` | 指定应使用沙特阿拉伯王国、伊斯兰事务、捐赠、宣教和指导部所描述的伊斯兰历法。 |
| Japan | `8` | 指定应使用日本天皇纪年历，如 日本工业标准 JIS X 0301 所述。 |
| Korea | `9` | 指定应使用韩国法令第 4 号所描述的朝鲜檀君时代日历 。 |
| None | `10` | 指定不应使用日历。 |
| Saka | `11` | 指定应使用印度历法改革委员会所描述的萨卡时代历法（ ，作为印度星历和航海年历的一部分）。 |
| Taiwan | `12` | 指定应使用中国国家标准 CNS 7648 定义的台湾日历。 |
| Thai | `13` | 指定应使用泰国历法，该历法由泰国国王哇集拉兀 (拉玛六世) 在 皇家公报 BE 2456 (公元 1913 年) 中颁布的皇家法令以及泰国总理銮披汶颂堪 (Phibunsongkhram) 的法令 (公元 1941 年) 定义， 以公历 1 月 1 日为年份起点，将公历零年映射到公元前 543 年。 |

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
