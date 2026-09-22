---
title: "Aspose::Words::LowCode::Comparer class"
linktitle: "Comparer"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Comparer class. يوفر طرقًا تهدف إلى مقارنة المستندات في C++."
type: docs
weight: 500
url: /ar/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


يوفر طرقًا تهدف إلى مقارنة المستندات.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | يقارن مستندين ويحفظ الفروقات كصور. كل عنصر في المصفوفة المرتجعة يمثل صفحة واحدة من الإخراج المصوَّر كصورة. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن مستندين ويحفظ الفروقات كصور. كل عنصر في المصفوفة المرتجعة يمثل صفحة واحدة من الإخراج المصوَّر كصورة. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | يقارن مستندين ويحفظ الفروقات كصور. كل عنصر في المصفوفة المرتجعة يمثل صفحة واحدة من الإخراج المصوَّر كصورة. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | يقارن مستندين ويحفظ الفروقات كصور. كل عنصر في المصفوفة المرتجعة يمثل صفحة واحدة من الإخراج المصوَّر كصورة. |
| static [Create](./create/)() | ينشئ مثيلًا جديدًا لمعالج التحويل. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | ينشئ مثيلًا جديدًا لمعالج المقارنة. |
| [Execute](../processor/execute/)() | تنفيذ إجراء المعالج. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | تنفيذ إجراء المعالج مع السماح بإلغاء مهمة معالجة المستند باستخدام رمز الإلغاء المحدد. |
| [From](../processor/from/)(const System::String\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
