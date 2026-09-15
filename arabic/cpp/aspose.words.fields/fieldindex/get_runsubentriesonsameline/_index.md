---
title: "طريقة Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine. يحصل أو يضبط ما إذا كانت الإدخالات الفرعية تُوضع في نفس السطر مع الإدخال الرئيسي في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


يحصل أو يعيّن ما إذا كان يتم تشغيل الإدخالات الفرعية في نفس السطر مع الإدخال الرئيسي.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## أمثلة



يوضح كيفية العمل مع الإدخالات الفرعية في حقل INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حقل INDEX سيعرض مدخلاً لكل حقل XE يُعثر عليه في المستند.
// سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
// سيجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text".
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// حقول XE التي تحتوي على خاصية Text التي يصبح قيمتها عنوان إدخال INDEX.
// إذا كانت هذه القيمة تحتوي على جزأين من السلسلة مقسومين بنقطتين (:)، سيتعامل إدخال INDEX مع الفاصل :) ،
// الجزء الأول هو العنوان، والجزء الثاني سيصبح العنوان الفرعي.
// يقوم حقل INDEX أولاً بتجميع الإدخالات أبجدياً، ثم إذا كان هناك عدة حقول XE بنفس
// العناوين، سيقوم حقل INDEX بتقسيمها فرعياً وفقاً لقيم هذه العناوين.
// يمكن أن تكون هناك طبقات فرعية متعددة، اعتماداً على عدد المرات التي
// تُقسم فيها خصائص Text لحقول XE بهذه الطريقة.
// بشكل افتراضي، سيُنشئ مجموعة إدخالات حقل INDEX سطرًا جديدًا لكل عنوان فرعي داخل هذه المجموعة.
// يمكننا تعيين علامة RunSubentriesOnSameLine إلى true للحفاظ على العنوان،
// وكل عنوان فرعي للمجموعة في سطر واحد بدلاً من ذلك، مما يجعل حقل INDEX أكثر تجميعاً.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// أدرج حقلين XE، كل منهما في صفحة جديدة، وبنفس العنوان المسمى "Heading 1",
// الذي سيستخدمه حقل INDEX لتجميعهما.
// إذا كان RunSubentriesOnSameLine false، فإن جدول INDEX سيُنشئ ثلاثة أسطر:
// سطر واحد لعنوان التجميع "Heading 1"، وسطر إضافي لكل عنوان فرعي.
// إذا كان RunSubentriesOnSameLine true، فإن جدول INDEX سيُنشئ سطرًا واحدًا
// يحتوي على العنوان وكل العناوين الفرعية.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## انظر أيضًا

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
