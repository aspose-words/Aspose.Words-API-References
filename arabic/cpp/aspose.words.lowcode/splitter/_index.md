---
title: "فئة Aspose::Words::LowCode::Splitter"
linktitle: "Splitter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::LowCode::Splitter. يوفر طرقًا تهدف إلى تقسيم المستندات إلى أجزاء باستخدام معايير مختلفة في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


يوفر طرقًا تهدف إلى تقسيم المستندات إلى أجزاء باستخدام معايير مختلفة.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | ينشئ نسخة جديدة من معالج القسّم. |
| [Execute](../processor/execute/)() | تنفيذ إجراء المعالج. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | تنفيذ إجراء المعالج مع السماح بإلغاء مهمة معالجة المستند باستخدام رمز الإلغاء المحدد. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد. يتم تحديد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | يستخرج نطاقًا محددًا من الصفحات من تدفق المستند ويحفظ الصفحات المستخرجة إلى تدفق إخراج باستخدام تنسيق الحفظ المحدد. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | يستخرج نطاقًا محددًا من الصفحات من تدفق المستند ويحفظ الصفحات المستخرجة إلى تدفق إخراج باستخدام تنسيق الحفظ المحدد. |
| [From](../processor/from/)(const System::String\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | يزيل الصفحات الفارغة من المستند ويحفظ النتيجة. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | يزيل الصفحات الفارغة من المستند ويحفظ النتيجة بالتنسيق المحدد. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يزيل الصفحات الفارغة من المستند ويحفظ النتيجة بالتنسيق المحدد. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | يزيل الصفحات الفارغة من مستند مقدم عبر تدفق إدخال ويحفظ المستند المحدث إلى تدفق إخراج بالتنسيق المحدد للحفظ. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يزيل الصفحات الفارغة من مستند مقدم عبر تدفق إدخال ويحفظ المستند المحدث إلى تدفق إخراج بالتنسيق المحدد للحفظ. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | يقسم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة إلى ملفات. يتم تحديد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | يقسم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة إلى ملفات بالتنسيق المحدد للحفظ. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | يقسم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة إلى ملفات بالتنسيق المحدد للحفظ. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | يقسم مستندًا من تدفق إدخال إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويعيد الأجزاء الناتجة كمصفوفة من التدفقات بالتنسيق المحدد للحفظ. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | يقسم مستندًا من تدفق إدخال إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويعيد الأجزاء الناتجة كمصفوفة من التدفقات بالتنسيق المحدد للحفظ. |
| [To](../processor/to/)(const System::String\&) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يحدد تدفق الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | يحدد تدفق الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
