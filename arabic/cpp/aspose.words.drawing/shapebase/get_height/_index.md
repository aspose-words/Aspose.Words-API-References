---
title: "Aspose::Words::Drawing::ShapeBase::get_Height طريقة"
linktitle: "get_Height"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Height طريقة. يسترجع أو يعيّن ارتفاع كتلة الحاوية للشكل في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.drawing/shapebase/get_height/
---
## ShapeBase::get_Height method


يحصل أو يضبط ارتفاع الكتلة المحتوية على الشكل.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Height()
```

## ملاحظات


بالنسبة لشكل المستوى الأعلى، تكون القيمة بالنقاط.

بالنسبة للأشكال داخل مجموعة، تكون القيمة في مساحة الإحداثيات ووحدات المجموعة الأصلية.

القيمة الافتراضية هي 0.

## أمثلة



يُظهر كيفية إدراج صورة عائمة، وتحديد موضعها وحجمها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// قم بتكوين خاصية "RelativeHorizontalPosition" للشكل لتعامل مع قيمة خاصية "Left"
// كالمسافة الأفقية للشكل، بالنقاط، من الجانب الأيسر للصفحة.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// عيّن المسافة الأفقية للشكل من الجانب الأيسر للصفحة إلى 100.
shape->set_Left(100);

// استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لتحديد موضع الشكل 80 نقطة أسفل أعلى الصفحة.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// عيّن ارتفاع الشكل، والذي سيُعيد تحجيم العرض تلقائيًا للحفاظ على الأبعاد.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// خاصيتي "Bottom" و "Right" تحتويان على الحافة السفلية واليمنى للصورة.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
