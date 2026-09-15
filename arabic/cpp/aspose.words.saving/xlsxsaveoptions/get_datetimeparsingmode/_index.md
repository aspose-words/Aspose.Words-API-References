---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode method"
linktitle: "get_DateTimeParsingMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode method. يحصل أو يحدد الوضع الذي يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت. القيمة الافتراضية هي UseCurrentLocale في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


يحصل أو يحدد الوضع الذي يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت. القيمة الافتراضية هي [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


## أمثلة



يظهر كيفية تحديد الاكتشاف التلقائي لتنسيق التاريخ والوقت.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// حدد استخدام الاكتشاف التلقائي لتنسيق التاريخ والوقت.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## انظر أيضًا

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
