---
title: "Aspose::Words::Drawing::ImageSize klass"
linktitle: "ImageSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageSize klass. Innehåller information om bildstorlek och upplösning. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.drawing/imagesize/
---
## ImageSize class


Innehåller information om bildstorlek och upplösning. För att lära dig mer, besök dokumentationsartikeln [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageSize : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_HeightPixels](./get_heightpixels/)() const | Hämtar bildens höjd i pixlar. |
| [get_HeightPoints](./get_heightpoints/)() | Hämtar bildens höjd i punkter. 1 punkt är 1/72 tum. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Hämtar den horisontella upplösningen i DPI. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Hämtar den vertikala upplösningen i DPI. |
| [get_WidthPixels](./get_widthpixels/)() const | Hämtar bildens bredd i pixlar. |
| [get_WidthPoints](./get_widthpoints/)() | Hämtar bildens bredd i punkter. 1 punkt är 1/72 tum. |
| [GetType](./gettype/)() const override |  |
| [ImageSize](./imagesize/)(int32_t, int32_t) | Initierar bredd och höjd till de angivna värdena i pixlar. Initierar upplösning till 96 dpi. |
| [ImageSize](./imagesize/)(int32_t, int32_t, double, double) | Initierar bredd, höjd och upplösning till de angivna värdena. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man ändrar storlek på en form med en bild.
```cpp
// När vi infogar en bild med metoden "InsertImage" skalar byggaren formen som visar bilden så att,
// när vi visar dokumentet med 100% zoom i Microsoft Word, visar formen bilden i dess faktiska storlek.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// En 400x400 bild kommer att skapa ett ImageData-objekt med en bildstorlek på 300x300pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Om en forms dimensioner matchar bilddataens dimensioner,
// så visar formen bilden i sin ursprungliga storlek.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Minska den totala storleken på formen med 50 %.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// Skalfaktorer gäller både för bredden och höjden samtidigt för att bevara formens proportioner.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// När vi ändrar storlek på formen förblir bilddataens storlek densamma.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Vi kan referera till bilddataens dimensioner för att tillämpa en skalning baserad på bildens storlek.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
