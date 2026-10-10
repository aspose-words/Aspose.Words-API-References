---
title: "طريقة Aspose::Words::Drawing::ImageSize::get_WidthPoints"
linktitle: "get_WidthPoints"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ImageSize::get_WidthPoints. تحصل على عرض الصورة بالنقاط. النقطة الواحدة هي 1/72 بوصة في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing/imagesize/get_widthpoints/
---
## ImageSize::get_WidthPoints method


يحصل على عرض الصورة بالنقاط. 1 نقطة تساوي 1/72 بوصة.

```cpp
double Aspose::Words::Drawing::ImageSize::get_WidthPoints()
```


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

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
