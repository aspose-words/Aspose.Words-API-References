---
title: "Aspose::Words::Drawing::ShapeBase::get_Right metodu"
linktitle: "get_Right"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Right metodu. C++'da şeklin içinde bulunduğu bloğun sağ kenar konumunu alır."
type: docs
weight: 44000
url: /tr/cpp/aspose.words.drawing/shapebase/get_right/
---
## ShapeBase::get_Right method


Şeklin içinde bulunduğu bloğun sağ kenar konumunu alır.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Right()
```

## Açıklamalar


Üst düzey bir şekil için değer, puan cinsindendir ve şekil çapa noktasına göre görecelidir.

Bir grup içindeki şekiller için değer, ebeveyn grubunun koordinat uzayında ve birimlerinde bulunur.

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

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
