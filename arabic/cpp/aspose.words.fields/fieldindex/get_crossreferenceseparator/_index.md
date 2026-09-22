---
title: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator method"
linktitle: "get_CrossReferenceSeparator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator method. يحصل على أو يضبط تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة وغيرها من الإدخالات في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldindex/get_crossreferenceseparator/
---
## FieldIndex::get_CrossReferenceSeparator method


يحصل أو يعيّن تسلسل الأحرف المستخدم لفصل الإشارات المتقاطعة وغيرها من الإدخالات.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator()
```


## أمثلة



يظهر كيفية تعريف المراجع المتقاطعة في حقل INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حقل INDEX سيعرض مدخلاً لكل حقل XE يُعثر عليه في المستند.
// سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
// سيجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text".
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// يمكننا تكوين حقل XE لجعل إدخال INDEX الخاص به يعرض سلسلة بدلاً من رقم الصفحة.
// أولاً، بالنسبة للإدخالات التي تستبدل رقم الصفحة بسلسلة،
// حدد فاصلًا مخصصًا بين قيمة خاصية Text لحقل XE والسلسلة.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// أدرج حقل XE، الذي ينشئ إدخال INDEX عادي يعرض رقم صفحة هذا الحقل،
// ولا يستدعي قيمة CrossReferenceSeparator.
// سيعرض الإدخال لهذا الحقل XE "Apple, 2".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// أدرج حقل XE آخر في الصفحة 3 واضبط قيمة خاصية PageNumberReplacement.
// ستظهر هذه القيمة بدلاً من رقم الصفحة التي يقع عليها هذا الحقل،
// وقيمة CrossReferenceSeparator لحقل INDEX ستظهر أمامها.
// سيعرض الإدخال لهذا الحقل XE "Banana, see: Tropical fruit".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## انظر أيضًا

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
