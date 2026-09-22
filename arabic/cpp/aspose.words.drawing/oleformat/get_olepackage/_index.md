---
title: "Aspose::Words::Drawing::OleFormat::get_OlePackage طريقة"
linktitle: "get_OlePackage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::OleFormat::get_OlePackage طريقة. يوفر الوصول إلى OlePackage إذا كان كائن OLE هو حزمة OLE. يُرجِع **null** خلاف ذلك في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.drawing/oleformat/get_olepackage/
---
## OleFormat::get_OlePackage method


وفر الوصول إلى [OlePackage](../../olepackage/) إذا كان كائن OLE هو حزمة OLE. يُرجِع **null** خلاف ذلك.

```cpp
System::SharedPtr<Aspose::Words::Drawing::OlePackage> Aspose::Words::Drawing::OleFormat::get_OlePackage()
```


## أمثلة



يظهر كيفية إدراج كائن OLE في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تسمح كائنات OLE لنا بفتح ملفات أخرى في نظام الملفات المحلي باستخدام تطبيق مثبت آخر
// في نظام التشغيل الخاص بنا عن طريق النقر المزدوج على الشكل الذي يحتوي على كائن OLE في جسم المستند.
// في هذه الحالة، سيكون ملفنا الخارجي أرشيف ZIP.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## انظر أيضًا

* Class [OlePackage](../../olepackage/)
* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
