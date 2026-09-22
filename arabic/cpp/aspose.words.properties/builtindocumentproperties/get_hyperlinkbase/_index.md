---
title: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase"
linktitle: "get_HyperlinkBase"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase. تحدد السلسلة الأساسية المستخدمة لتقييم الروابط التشعبية النسبية في هذا المستند في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


يحدد السلسلة الأساسية المستخدمة لتقييم الروابط النسبية في هذا المستند.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## ملاحظات


لا يستخدم Aspose.Words هذه الخاصية.

## أمثلة



يوضح كيفية تخزين الجزء الأساسي من الرابط التشعبي في خصائص المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج رابطًا تشعبيًا نسبيًا إلى مستند في نظام الملفات المحلي باسم "Document.docx".
// النقر على الرابط في Microsoft Word سيفتح المستند المحدد إذا كان متاحًا.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// هذا الرابط نسبي. إذا لم يكن هناك "Document.docx" في نفس المجلد
// مع المستند الذي يحتوي على هذا الرابط، سيتعطل الرابط.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// المستند الذي نحاول الارتباط به موجود في دليل مختلف عن الدليل الذي نخطط لحفظ المستند فيه.
// يمكننا إصلاح الروابط بهذه الطريقة عن طريق وضع اسم ملف مطلق في كل منها.
// بدلاً من ذلك، يمكننا توفير رابط أساسي يضيفه كل رابط تشعبي يحتوي على اسم ملف نسبي
// سيُسبق إلى رابطها عندما نضغط عليه.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
