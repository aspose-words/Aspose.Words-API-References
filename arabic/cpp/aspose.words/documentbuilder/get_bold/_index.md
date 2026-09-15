---
title: "طريقة Aspose::Words::DocumentBuilder::get_Bold"
linktitle: "get_Bold"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::get_Bold. صحيحة إذا كان الخط مُنسقًا كغامق في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/documentbuilder/get_bold/
---
## DocumentBuilder::get_Bold method


صحيح إذا كان الخط مُنسقًا كغامق.

```cpp
bool Aspose::Words::DocumentBuilder::get_Bold()
```


## أمثلة



يظهر كيفية ملء حقول MERGEFIELD بالبيانات باستخدام مُنشئ المستند بدلاً من الدمج البريدي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج بعض حقول MERGEFIELD، التي تقبل البيانات من أعمدة ذات الاسم نفسه في مصدر البيانات أثناء الدمج البريدي،
// ثم قم بملئها يدويًا.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
