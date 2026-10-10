---
title: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture طريقة"
linktitle: "get_PreProcessCulture"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture طريقة. يحصل أو يعيّن الثقافة لمعالجة قيم الحقول مسبقًا في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


الحصول على أو تعيين الثقافة لمعالجة قيم الحقول مسبقًا.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## ملاحظات


حاليًا، هذه الخاصية تؤثر فقط على قيمة حقل [FieldDocProperty](../../fielddocproperty/).

القيمة الافتراضية هي **null**. عند تعيين هذه الخاصية إلى **null**, يتم معالجة قيمة حقل [FieldDocProperty](../../fielddocproperty/) مسبقًا باستخدام الثقافة التي يتحكم فيها خاصية [FieldUpdateCultureSource](../get_fieldupdateculturesource/).

## أمثلة



يظهر كيفية تعيين ثقافة المعالجة المسبقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عيّن الثقافة التي سيُنسق وفقًا لها بعض الحقول قيمها المعروضة.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// حقل DOCPROPERTY سيعرض نتيجته مُنسقة وفقًا لثقافة المعالجة المسبقة
// لقد قمنا بتعيينه إلى الألمانية. سيعرض الحقل التاريخ/الوقت باستخدام تنسيق "dd.mm.yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// بعد التحويل إلى الثقافة الثابتة، سيستخدم حقل DOCPROPERTY تنسيق "mm/dd/yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## انظر أيضًا

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
