---
title: "Aspose::Words::Fields::FieldAdvance::get_RightOffset طريقة"
linktitle: "get_RightOffset"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldAdvance::get_RightOffset طريقة. يحصل أو يضبط عدد النقاط التي يجب أن يتحرك النص الذي يلي الحقل إلى اليمين في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fields/fieldadvance/get_rightoffset/
---
## FieldAdvance::get_RightOffset method


يحصل أو يعيّن عدد النقاط التي يجب أن يتحرك بها النص الذي يلي الحقل إلى اليمين.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_RightOffset()
```


## أمثلة



يوضح كيفية إدراج حقل ADVANCE، وتعديل خصائصه.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// فيما يلي طريقتان لاستخدام حقل ADVANCE لضبط موضع النص الذي يليه.
// تستمر تأثيرات حقل ADVANCE في التطبيق حتى نهاية الفقرة،
// أو يقوم حقل ADVANCE آخر بتحديث قيم الإزاحة/الإحداثيات.
// 1 -  حدد إزاحة اتجاهية:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  انقل النص إلى موضع محدد بالإحداثيات:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## انظر أيضًا

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
