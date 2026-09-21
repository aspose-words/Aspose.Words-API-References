---
title: "Aspose::Words::Drawing::ImageSize::get_HorizontalResolution metod"
linktitle: "get_HorizontalResolution"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageSize::get_HorizontalResolution metod. Hämtar den horisontella upplösningen i DPI i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.drawing/imagesize/get_horizontalresolution/
---
## ImageSize::get_HorizontalResolution method


Hämtar den horisontella upplösningen i DPI.

```cpp
double Aspose::Words::Drawing::ImageSize::get_HorizontalResolution() const
```


## Exempel



Visar hur man läser egenskaperna för en bild i en form.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en form i dokumentet som innehåller en bild hämtad från vårt lokala filsystem.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Om formen innehåller en bild, kommer dess ImageData-egenskap att vara giltig,
// och den kommer att innehålla ett ImageSize-objekt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// ImageSize-objektet innehåller skrivskyddad information om bilden i formen.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// Vi kan basera storleken på formen på storleken på dess bild för att undvika att sträcka bilden.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## Se även

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
