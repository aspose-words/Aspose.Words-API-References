---
title: "طريقة Aspose::Words::Fields::FieldXE::get_Yomi"
linktitle: "get_Yomi"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldXE::get_Yomi. يحصل أو يضبط الـ yomi (الحرف الصوتي الأول لفرز الفهارس) لإدخال الفهرس في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.fields/fieldxe/get_yomi/
---
## FieldXE::get_Yomi method


يحصل أو يضبط الـ yomi (الحرف الصوتي الأول لفرز الفهارس) لإدخال الفهرس.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Yomi()
```


## أمثلة



يظهر كيفية فرز إدخالات حقل INDEX صوتيًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حقل INDEX سيعرض مدخلاً لكل حقل XE يُعثر عليه في المستند.
// سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
// سيجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text".
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// يقوم جدول INDEX بفرز إدخالاته تلقائيًا وفقًا لقيم خصائص Text الخاصة بها بترتيب أبجدي.
// قم بتعيين جدول INDEX لفرز الإدخالات صوتيًا باستخدام Hiragana بدلاً من ذلك.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// أدرج 4 حقول XE، والتي ستظهر كإدخالات في جدول محتويات حقل INDEX.
// قد تحتوي خاصية "Text" على تهجئة كلمة بالكانجي، والتي قد يكون نطقها غامضًا،
// في حين أن نسخة "Yomi" من الكلمة ستكتب بالضبط كما تُنطق باستخدام Hiragana.
// إذا قمنا بتعيين حقل INDEX لاستخدام Yomi، فسيتم فرز هذه الإدخالات
// حسب قيمة خصائص Yomi الخاصة بهم، بدلاً من قيم Text الخاصة بهم.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## انظر أيضًا

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
