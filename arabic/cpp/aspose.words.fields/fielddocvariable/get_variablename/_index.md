---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName طريقة"
linktitle: "get_VariableName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName طريقة. يحصل أو يعيّن اسم المتغيّر الوثائقي لاسترجاعه في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


يحصل أو يضبط اسم المتغيّر في المستند لاسترجاعه.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## أمثلة



يظهر كيفية استخدام حقول DOCPROPERTY لعرض خصائص المستند والمتغيرات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي طريقتان لاستخدام حقول DOCPROPERTY.
// 1 -  عرض خاصية مدمجة:
// عيّن قيمة مخصصة للخاصية المدمجة "Category"، ثم أدخل حقل DOCPROPERTY الذي يشير إليها.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  عرض متغير مستند مخصص:
// عرّف متغيرًا مخصصًا، ثم اشِر إلى ذلك المتغير باستخدام حقل DOCPROPERTY.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## انظر أيضًا

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
