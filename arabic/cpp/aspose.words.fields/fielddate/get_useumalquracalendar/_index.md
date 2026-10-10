---
title: "طريقة Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar. يحصل أو يضبط ما إذا كان سيتم استخدام تقويم أم القرى في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fields/fielddate/get_useumalquracalendar/
---
## FieldDate::get_UseUmAlQuraCalendar method


يحصل أو يضبط ما إذا كان سيتم استخدام تقويم أم القرى.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar() override
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
