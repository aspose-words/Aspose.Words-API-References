---
title: "طريقة Aspose::Words::Document::RemoveMacros"
linktitle: "RemoveMacros"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::RemoveMacros. يزيل جميع الماكروهات (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند في C++."
type: docs
weight: 69000
url: /ar/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


يزيل جميع الماكرو (مشروع VBA) بالإضافة إلى أشرطة الأدوات وتخصيصات الأوامر من المستند.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## ملاحظات


من خلال إزالة جميع الماكروهات من المستند يمكنك التأكد من أن المستند لا يحتوي على فيروسات ماكرو.

## أمثلة



يوضح كيفية إزالة جميع الماكروهات من المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// إزالة مشروع VBA الخاص بالمستند، جنبًا إلى جنب مع جميع ماكروه.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
