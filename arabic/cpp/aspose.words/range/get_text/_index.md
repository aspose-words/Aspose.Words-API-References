---
title: "طريقة Aspose::Words::Range::get_Text"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Range::get_Text. تحصل على نص النطاق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


يحصل على نص النطاق.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## ملاحظات


السلسلة المرتجعة تشمل جميع أحرف التحكم والأحرف الخاصة كما هو موضح في [ControlChar](../../controlchar/).

## أمثلة



يوضح كيفية الحصول على محتوى النص لجميع العقد التي يغطيها النطاق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## انظر أيضًا

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
