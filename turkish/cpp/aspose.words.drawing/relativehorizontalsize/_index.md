---
title: "Aspose::Words::Drawing::RelativeHorizontalSize enum"
linktitle: "RelativeHorizontalSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::RelativeHorizontalSize enum. Bir şeklin veya metin çerçevesinin genişliğinin C++'da yatay olarak neye göre hesaplandığını belirtir."
type: docs
weight: 33500
url: /tr/cpp/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enum


Bir şeklin veya metin çerçevesinin genişliğinin yatay olarak neye göre hesaplandığını belirtir.

```cpp
enum class RelativeHorizontalSize
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Kenar boşluğu | 0 | Genişliğin sol ve sağ kenar boşlukları arasındaki alana göre hesaplandığını belirtir. |
| Page | 1 | Genişliğin sayfa genişliğine göre hesaplandığını belirtir. |
| LeftMargin | 2 | Genişliğin sol kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| RightMargin | 3 | Genişliğin sağ kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| InnerMargin | 4 | Genişliğin iç kenar boşluğu alanı boyutuna göre, tek sayfalarda sol kenar boşluğu alanı boyutuna ve çift sayfalarda sağ kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| OuterMargin | 5 | Genişliğin dış kenar boşluğu alanı boyutuna göre, tek sayfalarda sağ kenar boşluğu alanı boyutuna ve çift sayfalarda sol kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| Default | n/a | Varsayılan değer [Margin](./) dir. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
