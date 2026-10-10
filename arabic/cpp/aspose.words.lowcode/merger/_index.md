---
title: "فئة Aspose::Words::LowCode::Merger"
linktitle: "Merger"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::LowCode::Merger. تمثل مجموعة من الطرق المقصود منها دمج مجموعة متنوعة من أنواع المستندات المختلفة في مستند إخراج واحد في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.lowcode/merger/
---
## Merger class


يمثل مجموعة من الطرق التي تهدف إلى دمج مجموعة متنوعة من أنواع المستندات في مستند إخراج واحد.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Create](./create/)() | ينشئ مثلاً جديداً لمعالج دمج البريد. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | ينشئ مثلاً جديداً لمعالج دمج البريد. |
| [Execute](../processor/execute/)() | تنفيذ إجراء المعالج. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | تنفيذ إجراء المعالج مع السماح بإلغاء مهمة معالجة المستند باستخدام رمز الإلغاء المحدد. |
| [From](../processor/from/)(const System::String\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام أسماء ملفات الإدخال والإخراج المحددة باستخدام [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام أسماء ملفات الإدخال والإخراج المحددة وتنسيق المستند النهائي. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند واحد ويعيد مثيل [Document](../../aspose.words/document/) للمستند النهائي. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند واحد ويعيد مثيل [Document](../../aspose.words/document/) للمستند النهائي. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند واحد ويعيد مثيل [Document](../../aspose.words/document/) للمستند النهائي. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة وتنسيق المستند النهائي. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة وخيارات الحفظ. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة وخيارات الحفظ. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند واحد ويعيد مثيل [Document](../../aspose.words/document/) للمستند النهائي. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند واحد ويعيد مثيل [Document](../../aspose.words/document/) للمستند النهائي. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ. يصوّر الإخراج إلى صور. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | يدمج تدفقات المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام خيارات حفظ الصور المحددة. يصوّر الإخراج إلى صور. |
| [To](../processor/to/)(const System::String\&) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | يحدد ملف الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يحدد تدفق الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | يحدد تدفق الإخراج للمعالج. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## ملاحظات


يتم استخدام ملفات أو تدفقات الإدخال والإخراج المحددة، إلى جانب خيارات الدمج والحفظ المطلوبة، لدمج المستندات الإدخالية المعطاة في مستند إخراج واحد.

تدعم وظيفة الدمج أكثر من 35 تنسيق ملف مختلف.
## انظر أيضًا

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
