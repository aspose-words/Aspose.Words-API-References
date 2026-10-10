---
title: "طريقة Aspose::Words::Fields::FieldXE::get_Text"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldXE::get_Text طريقة. يحصل أو يضبط نص الإدخال في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.fields/fieldxe/get_text/
---
## FieldXE::get_Text method


يحصل أو يضبط نص الإدخال.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Text()
```


## أمثلة



يظهر كيفية إنشاء حقل INDEX، ثم استخدام حقول XE لملئه بالمدخلات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حقل INDEX سيعرض مدخلاً لكل حقل XE يُعثر عليه في المستند.
// كل مدخل سيعرض قيمة خاصية Text لحقل XE على الجانب الأيسر
// والصفحة التي تحتوي على حقل XE على الجانب الأيمن.
// إذا كان لحقل XE نفس القيمة في خاصية "Text" الخاصة به،
// سوف يقوم حقل INDEX بتجميعها في مدخل واحد.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// قم بتكوين حقل INDEX لعرض حقول XE فقط التي تقع ضمن حدود
// إشارة مرجعية تسمى "MainBookmark"، والخصائص "EntryType" لها قيمة "A".
// بالنسبة لكل من حقول INDEX و XE، خاصية "EntryType" تستخدم فقط الحرف الأول من قيمتها النصية.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// في صفحة جديدة، ابدأ الإشارة المرجعية باسم يطابق القيمة
// لخاصية "BookmarkName" لحقل INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// حقل INDEX سيستقبل هذا المدخل لأنه داخل الإشارة المرجعية،
// ونوع مدخله يطابق أيضاً نوع مدخل حقل INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// أدرج حقل XE لن يظهر في INDEX لأن أنواع المدخلات لا تتطابق.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// أنهِ الإشارة المرجعية وأدرج حقل XE بعد ذلك.
// هو من نفس نوع حقل INDEX، لكنه لن يظهر
// لأنه خارج حدود الإشارة المرجعية.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```


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

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
