---
title: "طريقة Aspose::Words::Drawing::OlePackage::get_FileName"
linktitle: "get_FileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::OlePackage::get_FileName طريقة. يحصل أو يضبط اسم ملف حزمة OLE في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing/olepackage/get_filename/
---
## OlePackage::get_FileName method


يحصل أو يعيّن اسم ملف حزمة OLE.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_FileName() const
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

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
