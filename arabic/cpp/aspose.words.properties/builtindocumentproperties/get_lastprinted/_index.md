---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted طريقة"
linktitle: "get_LastPrinted"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted طريقة. يحصل أو يضبط التاريخ الذي تم فيه طباعة المستند آخر مرة بتوقيت UTC في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_lastprinted/
---
## BuiltInDocumentProperties::get_LastPrinted method


يحصل أو يضبط تاريخ آخر طباعة للمستند بتوقيت UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted()
```

## ملاحظات


بالنسبة للمستندات التي نشأت من تنسيق RTF، تُعيد هذه الخاصية الوقت المحلي لعملية الطباعة الأخيرة.

إذا لم يتم طباعة المستند أبدًا، ستُعيد هذه الخاصية القيمة DateTime.MinValue.

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

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
