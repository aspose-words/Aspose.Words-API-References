---
title: "فئة Aspose::Words::Drawing::OlePackage"
linktitle: "OlePackage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::OlePackage. تسمح بالوصول إلى خصائص حزمة OLE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


يسمح بالوصول إلى خصائص حزمة OLE. لمعرفة المزيد، زر مقالة الوثائق [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OlePackage : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | يحصل أو يعيّن اسم عرض حزمة OLE. |
| [get_FileName](./get_filename/)() const | يحصل أو يعيّن اسم ملف حزمة OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | محدد لـ [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | محدد لـ [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
