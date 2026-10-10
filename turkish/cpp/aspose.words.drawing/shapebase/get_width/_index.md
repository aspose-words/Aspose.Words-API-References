---
title: "Aspose::Words::Drawing::ShapeBase::get_Width metodu"
linktitle: "get_Width"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Width metodu. Şeklin içinde bulunduğu bloğun genişliğini alır veya ayarlar C++'de."
type: docs
weight: 54000
url: /tr/cpp/aspose.words.drawing/shapebase/get_width/
---
## ShapeBase::get_Width method


Şeklin içinde bulunduğu bloğun genişliğini alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Width()
```

## Açıklamalar


Üst düzey bir şekil için değer puan cinsindendir.

Bir grup içindeki şekiller için değer, ebeveyn grubunun koordinat uzayında ve birimlerinde bulunur.

Varsayılan değer 0'dır.

## Örnekler



Yüzen bir görüntünün nasıl ekleneceğini ve konumunun ve boyutunun nasıl belirtileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Şeklin "RelativeHorizontalPosition" özelliğini, "Left" özelliğinin değerini şeklin yatay uzaklığı olarak ele alacak şekilde yapılandırın
// sayfanın sol tarafından, nokta cinsinden, şeklin yatay uzaklığı olarak.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Şeklin sayfanın sol tarafından yatay uzaklığını 100'e ayarlayın.
shape->set_Left(100);

// "RelativeVerticalPosition" özelliğini benzer bir şekilde kullanarak şekli sayfanın üstünden 80pt aşağı konumlandırın.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Şeklin yüksekliğini ayarlayın; bu, boyutları korumak için genişliği otomatik olarak ölçeklendirecektir.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// "Bottom" ve "Right" özellikleri, görüntünün alt ve sağ kenarlarını içerir.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


Shows how to resize a shape with an image.
```cpp
// When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
// when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// A 400x400 image will create an ImageData object with an image size of 300x300pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// If a shape's dimensions match the image data's dimensions,
// then the shape is displaying the image in its original size.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Reduce the overall size of the shape by 50%.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// When we resize the shape, the size of the image data remains the same.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// We can reference the image data dimensions to apply a scaling based on the size of the image.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
