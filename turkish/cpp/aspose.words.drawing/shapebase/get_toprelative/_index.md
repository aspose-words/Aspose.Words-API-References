---
title: "Aspose::Words::Drawing::ShapeBase::get_TopRelative metodu"
linktitle: "get_TopRelative"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_TopRelative metodu. C++'ta şeklin yüzde olarak göreceli üst konumunu temsil eden değeri alır veya ayarlar."
type: docs
weight: 52500
url: /tr/cpp/aspose.words.drawing/shapebase/get_toprelative/
---
## ShapeBase::get_TopRelative method


Şeklin yüzde cinsinden göreceli üst konumunu temsil eden değeri alır veya ayarlar.

```cpp
float Aspose::Words::Drawing::ShapeBase::get_TopRelative()
```


## Örnekler



İlgili boyut ve konumu nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Mutlak boyut ve konuma sahip basit bir şekil ekleme.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// WrapType'ı WrapType.None olarak ayarlayın, çünkü Satır içi şekiller otomatik olarak mutlak birimlere dönüştürülür.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// İlgili yatay boyutu kontrol etme ve ayarlama.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Yatay boyut bağlamasını Margin'e ayarlama.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Genişliği Margin genişliğinin %50'sine ayarlama.
    shape->set_WidthRelative(50.0f);
}

// İlgili dikey boyutu kontrol etme ve ayarlama.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Dikey boyut bağlamasını Margin'e ayarlama.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Yüksekliği Margin yüksekliğinin %30'una ayarlama.
    shape->set_HeightRelative(30.0f);
}

// İlgili dikey konumu kontrol etme ve ayarlama.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // Konum bağlamasını TopMargin'e ayarlama.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // İlgili üst konumu TopMargin konumunun %30'una ayarlama.
    shape->set_TopRelative(30.0f);
}

// İlgili yatay konumu kontrol etme ve ayarlama.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Konum bağlamasını RightMargin'e ayarlama.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // İlgili konum değeri negatif olabilir.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
