---
title: "طريقة Aspose::Words::Properties::DocumentProperty::ToByteArray"
linktitle: "ToByteArray"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::DocumentProperty::ToByteArray. تُرجع قيمة الخاصية كمصفوفة بايت في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


يعيد قيمة الخاصية كمصفوفة بايت.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## ملاحظات


يرمي استثناءً إذا لم يكن نوع الخاصية هو [ByteArray](../../propertytype/).

## أمثلة



يوضح كيفية إضافة صورة مصغرة إلى مستند نحفظه كملف Epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// إذا حفظنا مستندًا، حيث تحتوي خاصية "Thumbnail" على بيانات الصورة التي أضفناها، كملف Epub،
// قد يعرض القارئ الذي يفتح ذلك المستند الصورة قبل الصفحة الأولى.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// يمكننا استخراج صورة المصغرة للمستند وحفظها في نظام الملفات المحلي.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## انظر أيضًا

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
