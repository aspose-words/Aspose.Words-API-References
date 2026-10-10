---
title: "طريقة Aspose::Words::ControlChar::Tab"
linktitle: "علامة تبويب"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ControlChar::Tab. حرف Tab: \"\\x0009\" أو \"\\t\" في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/controlchar/tab/
---
## ControlChar::Tab method


حرف الجدولة: "\x0009" أو "\t".

```cpp
static System::String & Aspose::Words::ControlChar::Tab()
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

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
