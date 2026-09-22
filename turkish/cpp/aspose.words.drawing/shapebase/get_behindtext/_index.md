---
title: "Aspose::Words::Drawing::ShapeBase::get_BehindText metodu"
linktitle: "get_BehindText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_BehindText metodu. C++'ta şeklin metnin altında mı yoksa üstünde mi olduğunu belirtir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.drawing/shapebase/get_behindtext/
---
## ShapeBase::get_BehindText method


Şeklin metnin altında mı yoksa üstünde mi olduğunu belirtir.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_BehindText()
```

## Açıklamalar


Yalnızca üst düzey şekiller için etkilidir.

Varsayılan değer **false**'tur.

## Örnekler



Sayfanın ortasına yüzen bir görüntünün nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Üst üste gelen metnin arkasında görünecek bir yüzen görüntü ekleyin ve sayfanın ortasına hizalayın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
