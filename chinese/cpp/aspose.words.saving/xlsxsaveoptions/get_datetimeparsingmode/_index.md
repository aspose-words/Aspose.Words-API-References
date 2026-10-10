---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode 方法"
linktitle: "get_DateTimeParsingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode 方法。获取或设置指定如何解析文档文本以识别日期和时间值的模式。默认值在 C++ 中为 UseCurrentLocale。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


获取或设置指定如何解析文档文本以识别日期和时间值的模式。默认值为 [UseCurrentLocale](../../xlsxdatetimeparsingmode/)。

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


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

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
