---
title: "طريقة Aspose::Words::Fields::FieldIndex::get_EntryType"
linktitle: "get_EntryType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldIndex::get_EntryType. تحصل أو تعيين نوع إدخال الفهرس المستخدم لبناء الفهرس في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/fieldindex/get_entrytype/
---
## FieldIndex::get_EntryType method


يحصل أو يعيّن نوع إدخال الفهرس المستخدم لبناء الفهرس.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_EntryType()
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

## انظر أيضًا

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
