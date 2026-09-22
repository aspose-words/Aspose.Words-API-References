---
title: "Aspose::Words::Drawing::ImageData::get_ImageBytes طريقة"
linktitle: "get_ImageBytes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ImageData::get_ImageBytes طريقة. يحصل على أو يضبط البايتات الخام للصورة المخزنة في الشكل في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


يحصل أو يعيّن البايتات الخام للصورة المخزنة في الشكل.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## ملاحظات


ضبط القيمة إلى **null** أو مصفوفة فارغة سيزيل الصورة من الشكل.

تُرجع **null** إذا لم تكن الصورة مخزنة في المستند (مثلاً قد تكون الصورة مرتبطة في هذه الحالة).

## أمثلة



يوضح كيفية إنشاء ملف صورة من بيانات الصورة الخام للشكل.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() تُعيد المصفوفة المخزنة في الخاصية ImageBytes.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// احفظ بيانات صورة الشكل في ملف صورة على نظام الملفات المحلي.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## انظر أيضًا

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
