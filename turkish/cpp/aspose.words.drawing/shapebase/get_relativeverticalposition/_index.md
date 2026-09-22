---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition yöntemi"
linktitle: "get_RelativeVerticalPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition yöntemi. Şeklin dikey olarak neye göre konumlandırıldığını C++'ta belirtir."
type: docs
weight: 43000
url: /tr/cpp/aspose.words.drawing/shapebase/get_relativeverticalposition/
---
## ShapeBase::get_RelativeVerticalPosition method


Şeklin dikey olarak neye göre konumlandırıldığını belirtir.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition()
```

## Açıklamalar


Varsayılan değer [Paragraph](../../relativeverticalposition/) dir.

Yalnızca üst düzey yüzen şekiller için etkili olur.

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

* Enum [RelativeVerticalPosition](../../relativeverticalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
