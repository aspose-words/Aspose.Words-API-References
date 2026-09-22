---
title: "Aspose::Words::Drawing::ImageSize sınıfı"
linktitle: "ImageSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageSize sınıfı. Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir. Daha fazla bilgi için C++'daki belgeler makalesini ziyaret edin."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.drawing/imagesize/
---
## ImageSize class


Görüntü boyutu ve çözünürlüğü hakkında bilgi içerir. Daha fazla bilgi edinmek için [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/) dokümantasyon makalesini ziyaret edin.

```cpp
class ImageSize : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_HeightPixels](./get_heightpixels/)() const | Görüntünün yüksekliğini piksel cinsinden alır. |
| [get_HeightPoints](./get_heightpoints/)() | Görüntünün yüksekliğini puan cinsinden alır. 1 puan 1/72 inçtir. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Yatay çözünürlüğü DPI cinsinden alır. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Dikey çözünürlüğü DPI cinsinden alır. |
| [get_WidthPixels](./get_widthpixels/)() const | Görüntünün genişliğini piksel cinsinden alır. |
| [get_WidthPoints](./get_widthpoints/)() | Görüntünün genişliğini puan cinsinden alır. 1 puan 1/72 inçtir. |
| [GetType](./gettype/)() const override |  |
| [ImageSize](./imagesize/)(int32_t, int32_t) | Genişlik ve yüksekliği verilen değerlerle piksel cinsinden başlatır. Çözünürlüğü 96 DPI olarak başlatır. |
| [ImageSize](./imagesize/)(int32_t, int32_t, double, double) | Genişlik, yükseklik ve çözünürlüğü verilen değerlerle başlatır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Örnekler



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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
