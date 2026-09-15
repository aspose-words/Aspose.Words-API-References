---
title: "Aspose::Words::Drawing::ImageData::ToStream طريقة"
linktitle: "ToStream"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ImageData::ToStream طريقة. ينشئ ويعيد تدفقًا يحتوي على بايتات الصورة في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


ينشئ ويرجع دفقًا يحتوي على بايتات الصورة.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## ملاحظات


إذا كانت بايتات الصورة مخزنة في الشكل، ينشئ ويعيد كائن **MemoryStream**.

إذا كانت الصورة مرتبطة ومخزنة في ملف، يفتح الملف ويعيد كائن **FileStream**.

إذا كانت الصورة مرتبطة ومخزنة في عنوان URL خارجي، يقوم بتنزيل الملف ويعيد كائن **MemoryStream**.

هل هي مسؤولية المستدعي التخلص من كائن الدفق.

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
