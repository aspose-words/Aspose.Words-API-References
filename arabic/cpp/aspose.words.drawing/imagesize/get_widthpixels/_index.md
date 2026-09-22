---
title: "طريقة Aspose::Words::Drawing::ImageSize::get_WidthPixels"
linktitle: "get_WidthPixels"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ImageSize::get_WidthPixels method. يحصل على عرض الصورة بالبكسل في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing/imagesize/get_widthpixels/
---
## ImageSize::get_WidthPixels method


يحصل على عرض الصورة بالبكسل.

```cpp
int32_t Aspose::Words::Drawing::ImageSize::get_WidthPixels() const
```


## أمثلة



يظهر كيفية قراءة خصائص صورة داخل شكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج شكلاً في المستند يحتوي على صورة مأخوذة من نظام الملفات المحلي.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// إذا كان الشكل يحتوي على صورة، فستكون خاصية ImageData صالحة،
// وستحتوي على كائن ImageSize.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// كائن ImageSize يحتوي على معلومات للقراءة فقط حول الصورة داخل الشكل.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// يمكننا تحديد حجم الشكل بناءً على حجم صورته لتجنب تمديد الصورة.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## انظر أيضًا

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
