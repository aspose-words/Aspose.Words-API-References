---
title: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters"
linktitle: "get_Characters"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters. تمثّل تقديرًا لعدد الأحرف في المستند في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_characters/
---
## BuiltInDocumentProperties::get_Characters method


يمثل تقديرًا لعدد الأحرف في المستند.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters()
```

## ملاحظات


Aspose.Words يقوم بتحديث هذه الخاصية عندما تستدعي [UpdateWordCount](../../../aspose.words/document/updatewordcount/).

## أمثلة



يوضح كيفية تحديث جميع تسميات القوائم في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// لا يتتبع Aspose.Words مقاييس المستند مثل هذه في الوقت الفعلي.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// للحصول على قيم دقيقة لثلاثة من هذه الخصائص، سنحتاج إلى تحديثها يدويًا.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// لعدد الأسطر، سنحتاج إلى استدعاء تحميل زائد محدد لطريقة التحديث.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
