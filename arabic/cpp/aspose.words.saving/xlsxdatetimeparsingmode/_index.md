---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت في C++."
type: docs
weight: 86500
url: /ar/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت.

```cpp
enum class XlsxDateTimeParsingMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| UseCurrentLocale | 0 | يُستخدم تنسيق التاريخ والوقت المحدد للخيط الحالي أولاً لتحليل قيم السلسلة. إذا فشل التحليل، يتم تجربة تنسيقات تاريخ ووقت شائعة أخرى. |
| تلقائي | 1 | يتم تحديد تنسيق التاريخ والوقت المستخدم في المستند تلقائيًا. قد يستغرق ذلك وقتًا إضافيًا. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
