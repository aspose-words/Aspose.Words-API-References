---
title: "Aspose::Words::Markup::SdtCalendarType 枚举"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::SdtCalendarType 枚举。指定可在 C++ 中的 Office Open XML 文档中用于指定 CalendarType 的可能日历类型。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


指定可在 Office Open XML 文档中用于指定 [CalendarType](../structureddocumenttag/get_calendartype/) 的可能日历类型。

```cpp
enum class SdtCalendarType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Default | 0 | 在 OOXML 中用作默认值。等于 [Gregorian](./)。 |
| Gregorian | n/a | 指定应使用 ISO 8601 中定义的公历（Gregorian）日历。此日历应本地化为相应的语言。 |
| GregorianArabic | n/a | 指定使用 ISO 8601 中定义的公历。此日历的数值应以阿拉伯语显示。 |
| GregorianMeFrench | n/a | 指定使用 ISO 8601 中定义的公历。此日历的数值应以中东法语显示。 |
| GregorianUs | n/a | 指定使用 ISO 8601 中定义的公历。此日历的数值应以英语显示。 |
| GregorianXlitEnglish | n/a | 指定使用 ISO 8601 中定义的公历。此日历的数值应为英文字符串对应的阿拉伯字符表示（即公历英文的阿拉伯语音译）。 |
| GregorianXlitFrench | n/a | 指定使用 ISO 8601 中定义的公历。此日历的数值应为法文字符串对应的阿拉伯字符表示（即公历法文的阿拉伯语音译）。 |
| 希伯来语 | n/a | 指定使用希伯来阴历，依据逾越节的高斯公式 [CITATION] 和《口传律全书》（Mishneh Torah）描述的方式。 |
| Hijri | n/a | 指定使用伊斯兰阴历，依据沙特阿拉伯王国伊斯兰事务、捐赠、宣传与指导部的描述。 |
| Japan | n/a | 指定使用日本皇帝纪年历，依据日本工业标准 JIS X 0301 的描述。 |
| Korea | n/a | 指定使用韩国檀君纪元历，依据韩国法律第4号的规定。 |
| None | n/a | 指定不使用任何日历。 |
| Saka | n/a | 指定使用萨卡纪元历，依据印度日历改革委员会在《印度星历与航海年鉴》中的描述。 |
| Taiwan | n/a | 指定使用台湾日历，依据中国国家标准 CNS 7648 的定义。 |
| 泰语 | n/a | 指定使用泰国历，依据瓦集拉武国王（拉玛六世）在《皇家公报》B.E. 2456（公元1913年）颁布的皇家法令以及披武松卡姆总理（公元1941年）的法令，将年份起始设为公历1月1日，并将零年映射为公历前543年。 |


## 示例



展示如何使用结构化文档标签提示用户输入日期。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入一个提示用户输入日期的结构化文档标签。
// 在 Microsoft Word 中，此元素称为 "Date picker content control"。
// 当我们在 Microsoft Word 中点击此标签右端的箭头时，
// 我们会看到一个可点击的日历形式的弹出窗口。
// 我们可以使用该弹出窗口选择标签将显示的日期。
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// 根据沙特阿拉伯阿拉伯语地区设置显示日期。
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// 设置显示日期的格式。
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// 根据伊斯兰历显示日期。
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// 在用户在 Microsoft Word 中选择日期之前，标签将显示文本 "Click here to enter a date."。
// 根据标签的日历，设置 "FullDate" 属性以使标签显示默认日期。
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
