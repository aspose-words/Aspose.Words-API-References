---
title: "طريقة Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter"
linktitle: "get_SeparatorCharacter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter. تحصل أو تعيين حرف الفاصل الذي سيُستخدم في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


يحصل أو يضبط حرف الفاصل المستخدم.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## أمثلة



يعرض كيفية ترقيم الفقرات باستخدام حقول autonum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يعرض كل حقل AUTONUM القيمة الحالية لعدد متسلسل من حقول AUTONUM،
// مما يسمح لنا بترقيم العناصر تلقائيًا مثل قائمة مرقمة.
// سيعرض هذا الحقل الرقم "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// حرف الفاصل، الذي يظهر في نتيجة الحقل مباشرةً بعد الرقم، هو نقطة افتراضيًا.
// إذا تركنا هذه الخاصية فارغة، سيعرض حقل AUTONUM الثاني "2." في المستند.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// يمكننا ضبط هذه الخاصية لتطبيق الحرف الأول من سلسلته كحرف الفاصل الجديد.
// في هذه الحالة، سيعرض حقل AUTONUM الآن "2:".
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## انظر أيضًا

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
