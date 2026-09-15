---
title: "طريقة Aspose::Words::Drawing::ImageData::get_ImageSize"
linktitle: "get_ImageSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ImageData::get_ImageSize. يحصل على المعلومات حول حجم الصورة ودقتها في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.drawing/imagedata/get_imagesize/
---
## ImageData::get_ImageSize method


يحصل على المعلومات حول حجم الصورة ودقتها.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ImageSize> Aspose::Words::Drawing::ImageData::get_ImageSize()
```

## ملاحظات


إذا كانت الصورة مرتبطة فقط ولم تُخزن في المستند، تُعيد حجمًا صفرًا.

## أمثلة



يعرض كيفية تغيير حجم شكل باستخدام صورة.
```cpp
// عند إدراج صورة باستخدام طريقة "InsertImage"، يقوم المنشئ بتكبير الشكل الذي يعرض الصورة بحيث،
// عند عرض المستند باستخدام تكبير 100٪ في Microsoft Word، يعرض الشكل الصورة بحجمها الفعلي.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// ستنشئ صورة بحجم 400×400 كائن ImageData بحجم صورة 300×300 نقطة.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// إذا كانت أبعاد الشكل مطابقة لأبعاد بيانات الصورة،
// فإن الشكل يعرض الصورة بحجمها الأصلي.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// قلل الحجم الكلي للشكل بنسبة 50٪.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// تنطبق عوامل التحجيم على العرض والارتفاع في آنٍ واحد للحفاظ على نسب الشكل.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// عند تغيير حجم الشكل، يبقى حجم بيانات الصورة كما هو.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// يمكننا الرجوع إلى أبعاد بيانات الصورة لتطبيق تحجيم بناءً على حجم الصورة.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## انظر أيضًا

* Class [ImageSize](../../imagesize/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
