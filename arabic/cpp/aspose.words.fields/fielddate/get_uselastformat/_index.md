---
title: "طريقة Aspose::Words::Fields::FieldDate::get_UseLastFormat"
linktitle: "get_UseLastFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldDate::get_UseLastFormat. يحصل أو يضبط ما إذا كان سيتم استخدام تنسيق تم استخدامه آخرًا من قبل التطبيق المستضيف عند إدراج حقل DATE جديد في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fielddate/get_uselastformat/
---
## FieldDate::get_UseLastFormat method


يحصل أو يعيّن ما إذا كان سيُستخدم التنسيق الذي استخدمته آخر مرة من قبل التطبيق المستضيف عند إدراج حقل DATE جديد.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseLastFormat()
```


## أمثلة



يظهر كيفية استخدام حقول DATE لعرض التواريخ وفقًا لأنواع مختلفة من التقويمات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا أردنا أن يعرض النص في المستند دائمًا التاريخ الصحيح، يمكننا استخدام حقل DATE.
// فيما يلي ثلاثة أنواع من التقويمات الثقافية التي يمكن لحقل DATE استخدامها لعرض تاريخ.
// 1 -  التقويم القمري الإسلامي:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  تقويم أم القرى:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  التقويم الوطني الهندي:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// أدرج حقل DATE وحدد نوع تقويمه إلى النوع الذي استخدمه التطبيق المستضيف آخر مرة.
// في Microsoft Word، سيكون النوع هو الأكثر استخدامًا مؤخرًا في مربع الحوار إدراج -> نص -> تاريخ ووقت.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## انظر أيضًا

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
