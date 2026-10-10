---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. 指定在 C++ 中如何解析文档文本以识别日期和时间值。"
type: docs
weight: 86500
url: /zh/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


指定如何解析文档文本以识别日期和时间值。

```cpp
enum class XlsxDateTimeParsingMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| UseCurrentLocale | 0 | 首先使用为当前线程设置的日期时间格式来解析字符串值。如果解析失败，则尝试其他常见的日期时间格式。 |
| 自动 | 1 | 文档中使用的日期时间格式会自动确定。这可能会花费额外的时间。 |


## 示例



展示如何指定日期时间格式的自动检测。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// 指定使用日期时间格式的自动检测。
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
