---
title: "Aspose::Words::Drawing::ImageSize::get_HeightPixels yöntemi"
linktitle: "get_HeightPixels"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageSize::get_HeightPixels yöntemi. Görüntünün yüksekliğini piksel cinsinden C++'ta alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/imagesize/get_heightpixels/
---
## ImageSize::get_HeightPixels method


Görüntünün yüksekliğini piksel cinsinden alır.

```cpp
int32_t Aspose::Words::Drawing::ImageSize::get_HeightPixels() const
```


## Örnekler



Bir şekildeki görüntünün özelliklerini nasıl okuyacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yerel dosya sistemimizden alınan bir görüntüyü içeren bir şekli belgeye ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Şekil bir görüntü içeriyorsa, ImageData özelliği geçerli olacaktır,
// ve bir ImageSize nesnesi içerecektir.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// ImageSize nesnesi, şekil içindeki görüntü hakkında yalnızca okunabilir bilgi içerir.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// Görüntünün uzamasını önlemek için şeklin boyutunu görüntünün boyutuna göre ayarlayabiliriz.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## Ayrıca Bakınız

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
