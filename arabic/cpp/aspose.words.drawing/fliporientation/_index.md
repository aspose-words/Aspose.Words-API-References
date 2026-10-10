---
title: "Aspose::Words::Drawing::FlipOrientation enum"
linktitle: "FlipOrientation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::FlipOrientation enum. القيم المحتملة لتوجيه الشكل في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


القيم المحتملة لاتجاه الشكل.

```cpp
enum class FlipOrientation
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | الإحداثيات غير مقلوبة. |
| أفقي | 1 | قلب على المحور ص، مع عكس إحداثيات س. |
| عمودي | 2 | قلب على المحور س، مع عكس إحداثيات ص. |
| Both | 3 | قلب على كل من المحور ص والمحور س. |


## أمثلة



يظهر كيفية قلب شكل على محور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج شكلاً صورة واترك توجيهه في حالته الافتراضية.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// اضبط خاصية \"FlipOrientation\" إلى \"FlipOrientation.Horizontal\" لقلب الشكل الثاني على المحور ص،
// مما يجعله صورة مرآة أفقية للشكل الأول.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// اضبط خاصية \"FlipOrientation\" إلى \"FlipOrientation.Horizontal\" لقلب الشكل الثالث على المحور س،
// مما يجعله صورة مرآة عمودية للشكل الأول.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// اضبط خاصية \"FlipOrientation\" إلى \"FlipOrientation.Horizontal\" لقلب الشكل الرابع على كل من المحور س والمحور ص،
// مما يجعله صورة مرآة أفقية وعمودية للشكل الأول.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
