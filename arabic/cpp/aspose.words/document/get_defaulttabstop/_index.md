---
title: "Aspose::Words::Document::get_DefaultTabStop طريقة"
linktitle: "get_DefaultTabStop"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::get_DefaultTabStop طريقة. يحصل على أو يحدد الفاصل (بالنقاط) بين نقاط التبويب الافتراضية في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


يحصل أو يضبط الفاصل (بالنقاط) بين نقاط التبويب الافتراضية.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
```


## أمثلة



يظهر كيفية تعيين فاصل مخصص لمواقع نقاط التبويب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عيّن نقاط التبويب لتظهر كل 72 نقطة (1 بوصة).
builder->get_Document()->set_DefaultTabStop(72);

// كل حرف تبويب يثبت النص بعده إلى أقرب موقع نقطة تبويب.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
