---
title: "فئة Aspose::Words::Drawing::ImageSize"
linktitle: "ImageSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::ImageSize. تحتوي على معلومات حول حجم الصورة ودقتها. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing/imagesize/
---
## ImageSize class


يحتوي على معلومات حول حجم الصورة ودقتها. لمعرفة المزيد، زر مقالة الوثائق [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageSize : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_HeightPixels](./get_heightpixels/)() const | يحصل على ارتفاع الصورة بالبكسل. |
| [get_HeightPoints](./get_heightpoints/)() | يحصل على ارتفاع الصورة بالنقاط. 1 نقطة تساوي 1/72 بوصة. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | يحصل على الدقة الأفقية بوحدة DPI. |
| [get_VerticalResolution](./get_verticalresolution/)() const | يحصل على الدقة العمودية بوحدة DPI. |
| [get_WidthPixels](./get_widthpixels/)() const | يحصل على عرض الصورة بالبكسل. |
| [get_WidthPoints](./get_widthpoints/)() | يحصل على عرض الصورة بالنقاط. 1 نقطة تساوي 1/72 بوصة. |
| [GetType](./gettype/)() const override |  |
| [ImageSize](./imagesize/)(int32_t, int32_t) | يُهيئ العرض والارتفاع إلى القيم المعطاة بالبكسل. يُهيئ الدقة إلى 96 dpi. |
| [ImageSize](./imagesize/)(int32_t, int32_t, double, double) | يُهيئ العرض والارتفاع والدقة إلى القيم المعطاة. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
