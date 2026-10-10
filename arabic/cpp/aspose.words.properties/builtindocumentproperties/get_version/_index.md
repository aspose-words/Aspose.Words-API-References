---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Version طريقة"
linktitle: "get_Version"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Version طريقة. يمثل رقم الإصدار للتطبيق الذي أنشأ المستند في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_version/
---
## BuiltInDocumentProperties::get_Version method


يمثل رقم الإصدار للتطبيق الذي أنشأ المستند.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Version()
```

## ملاحظات


عندما يتم إنشاء مستند بواسطة Microsoft Word، فإن الـ 16 بت العليا تمثل الإصدار الرئيسي والـ 16 بت السفلى تمثل رقم البناء.

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

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
