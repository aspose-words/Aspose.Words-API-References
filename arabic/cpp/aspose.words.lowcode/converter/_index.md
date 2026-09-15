---
title: "فئة Aspose::Words::LowCode::Converter"
linktitle: "Converter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::LowCode::Converter. تمثل مجموعة من الطرق المقصودة لتحويل مجموعة متنوعة من أنواع المستندات باستخدام سطر واحد من الكود في C++."
type: docs
weight: 600
url: /ar/cpp/aspose.words.lowcode/converter/
---
## Converter class


يمثل مجموعة من الطرق التي تهدف إلى تحويل مجموعة متنوعة من أنواع المستندات باستخدام سطر واحد من الشيفرة.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | يحوِّل المستند المدخل المحدد إلى المستند الناتج باستخدام أسماء ملفات الإدخال والإخراج المحددة وامتداداتها. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وتنسيق المستند النهائي. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات التحميل/الحفظ الخاصة به. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | يقوم بتحويل المستند الإدخالي المعطى إلى مستند إخراجي واحد باستخدام تدفقات الإدخال والإخراج المحددة. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يقوم بتحويل المستند الإدخالي المعطى إلى مستند إخراجي واحد باستخدام تدفقات الإدخال والإخراج المحددة. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يقوم بتحويل المستند الإدخالي المعطى إلى مستند إخراجي واحد باستخدام تدفقات الإدخال والإخراج المحددة. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة بالتنسيق المحدد. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات الحفظ المحددة. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات التحميل والحفظ المقدمة. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات التحميل والحفظ المقدمة، ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | يقوم بتحويل صفحات المستند المحدد إلى صور بالتنسيق المحدد ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | يقوم بتحويل صفحات المستند المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| static [Create](./create/)() | ينشئ مثيلًا جديدًا لمعالج التحويل. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | ينشئ مثيلًا جديدًا لمعالج التحويل. |
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
## ملاحظات


يتم استخدام ملفات أو تدفقات الإدخال والإخراج المحددة، إلى جانب تنسيق الحفظ المطلوب، لتحويل المستند الإدخالي المعطى من تنسيق إلى المستند الإخراجي بالتنسيق المحدد الآخر.

تدعم وظيفة التحويل أكثر من 35 تنسيق ملف مختلف.

مجموعة الطرق [ConvertToImages()](../) مصممة لتحويل المستندات إلى صور، حيث يتم تحويل كل صفحة إلى ملف صورة منفصل. كما تقوم هذه الطرق بتحويل مستندات PDF مباشرة إلى تنسيقات صفحات ثابتة دون تحميلها إلى نموذج المستند، مما يعزز كلًا من الأداء والدقة.

باستخدام [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/)، يمكنك تحديد مجموعة معينة من الصفحات لتحويلها إلى صور.
## انظر أيضًا

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
