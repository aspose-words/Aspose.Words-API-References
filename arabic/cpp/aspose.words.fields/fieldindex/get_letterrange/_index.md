---
title: "Aspose::Words::Fields::FieldIndex::get_LetterRange طريقة"
linktitle: "get_LetterRange"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldIndex::get_LetterRange. تحصل أو تعيين نطاق من الحروف لتحديد الفهرس في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.fields/fieldindex/get_letterrange/
---
## FieldIndex::get_LetterRange method


يحصل أو يعيّن نطاق الحروف التي يحدّ الفهرس إليها.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_LetterRange()
```


## أمثلة



يظهر كيفية ملء حقل INDEX بالمدخلات باستخدام حقول XE، وكذلك تعديل مظهره.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حقل INDEX سيعرض مدخلاً لكل حقل XE يُعثر عليه في المستند.
// سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
// إذا كان لحقل XE نفس القيمة في خاصية "Text" الخاصة به،
// سوف يقوم حقل INDEX بتجميعها في مدخل واحد.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// ضبط قيمة هذه الخاصية إلى "A" سيقوم بتجميع جميع الإدخالات حسب حرفها الأول،
// وضع ذلك الحرف بالحروف الكبيرة فوق كل مجموعة.
index->set_Heading(u"A");

// حدد الجدول الذي أنشأه حقل INDEX ليغطي عمودين.
index->set_NumberOfColumns(u"2");

// حدد أي إدخالات تبدأ بحروف خارج النطاق "a-c" لتُحذف.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// ستظهر الحقلين التاليين من نوع XE تحت عنوان "A"،
// مع تطبيق تنسيقات النص الخاصة بهما أيضًا على أرقام الصفحات.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// كلا الحقلين التاليين من نوع XE سيكونان تحت عناوين "B" و "C" في فهرس جدول محتويات حقول INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// حقول INDEX تقوم بترتيب جميع الإدخالات أبجديًا، لذا سيظهر هذا الإدخال تحت "A" مع الإدخالين الآخرين.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// هذا الإدخال لن يظهر لأنه يبدأ بالحرف "D"،
// وهو خارج النطاق "a-c" الذي تحدده خاصية LetterRange لحقل INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## انظر أيضًا

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
