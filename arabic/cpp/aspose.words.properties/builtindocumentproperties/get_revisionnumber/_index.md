---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber طريقة"
linktitle: "get_RevisionNumber"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber. يحصل على أو يحدد رقم مراجعة المستند في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_revisionnumber/
---
## BuiltInDocumentProperties::get_RevisionNumber method


يحصل أو يضبط رقم مراجعة المستند.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber()
```

## ملاحظات


Aspose.Words لا يقوم بتحديث هذه الخاصية.

## أمثلة



يظهر كيفية العمل مع خصائص المستند في فئة "Origin".
```cpp
// افتح مستندًا قمنا بإنشائه وتحريره باستخدام Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// الخصائص المدمجة التالية تحتوي على معلومات حول إنشاء وتحرير هذا المستند.
// يمكننا النقر بزر الماوس الأيمن على هذا المستند في Windows Explorer والعثور على
// هذه الخصائص عبر "Properties" -> "Details" -> فئة "Origin".
// يمكن للحقول مثل PRINTDATE و EDITTIME عرض هذه القيم في جسم المستند.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// يمكننا أيضًا تغيير قيم الخصائص المدمجة.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word يقوم بتحديث الخصائص التالية تلقائيًا عند حفظ المستند.
// لاستخدام هذه الخصائص مع Aspose.Words، سنحتاج إلى ضبط القيم لها يدويًا.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// يمكننا النقر بزر الماوس الأيمن على هذا المستند في Windows Explorer والعثور على هذه الخصائص في "Properties" -> "Details" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```


يوضح كيفية العمل مع حقول REVNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Current revision #");

// أدرج حقل REVNUM، الذي يعرض خاصية رقم المراجعة الحالي للمستند.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRevNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRevisionNum, true));

ASSERT_EQ(u" REVNUM ", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_RevisionNumber());

// هذه الخاصية تحسب عدد مرات حفظ المستند في Microsoft Word،
// وهي غير مرتبطة بالمراجعات المتعقبة. يمكننا العثور عليها بالنقر بزر الماوس الأيمن على المستند في Windows Explorer
// من خلال الخصائص -> التفاصيل. يمكننا تحديث هذه الخاصية يدويًا.
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LVAL_LAMBDA_ARGS(doc->get_BuiltInDocumentProperties(), RevisionNumber));
field->Update();

ASSERT_EQ(u"2", field->get_Result());
```

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
