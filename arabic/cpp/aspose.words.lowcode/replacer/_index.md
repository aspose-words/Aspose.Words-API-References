---
title: "Aspose::Words::LowCode::Replacer class"
linktitle: "Replacer"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Replacer class. يوفر طرقًا تهدف إلى العثور على النص واستبداله في المستند في C++."
type: docs
weight: 1250
url: /ar/cpp/aspose.words.lowcode/replacer/
---
## Replacer class


يوفر طرقًا تهدف إلى العثور على النص واستبداله في المستند.

```cpp
class Replacer : public Aspose::Words::LowCode::Processor
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ReplacerContext\>\&) | ينشئ نسخة جديدة من معالج الاستبدال. |
| [Execute](../processor/execute/)() | تنفيذ إجراء المعالج. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | تنفيذ إجراء المعالج مع السماح بإلغاء مهمة معالجة المستند باستخدام رمز الإلغاء المحدد. |
| [From](../processor/from/)(const System::String\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | يحدد المستند الإدخالي للمعالجة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور. |
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
