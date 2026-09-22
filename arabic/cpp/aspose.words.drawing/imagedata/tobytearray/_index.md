---
title: "Aspose::Words::Drawing::ImageData::ToByteArray طريقة"
linktitle: "ToByteArray"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ImageData::ToByteArray طريقة. تُرجع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة في C++."
type: docs
weight: 36000
url: /ar/cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


يرجع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## ملاحظات


إذا كانت الصورة مرتبطة، يتم تنزيل الصورة في كل مرة يتم استدعاؤها.

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
