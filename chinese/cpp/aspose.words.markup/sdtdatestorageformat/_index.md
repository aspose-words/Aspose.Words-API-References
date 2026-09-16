---
title: "Aspose::Words::Markup::SdtDateStorageFormat 枚举"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::SdtDateStorageFormat 枚举。指定当 SDT 绑定到文档''的 XML 节点数据存储时，日期 SDT 的日期如何存储/检索（C++）。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


指定当日期 SDT 绑定到文档数据存储中的 XML 节点时，日期的存储/检索方式。

```cpp
enum class SdtDateStorageFormat
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 日期 | 0 | 日期 SDT 的日期值以标准 XML Schema 日期格式存储为日期。 |
| 日期时间 | 1 | 日期 SDT 的日期值以标准 XML Schema 日期时间格式存储为日期。 |
| 文本 | 2 | 日期 SDT 的日期值以文本形式存储。 |
| Default | n/a | 默认值为 [DateTime](./) |


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
