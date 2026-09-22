---
title: "Aspose::Words::Drawing::WrapType enum"
linktitle: "WrapType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::WrapType enum. Metnin C++'da bir şekil veya resim etrafında nasıl sarıldığını belirtir."
type: docs
weight: 45000
url: /tr/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Metnin bir şekil veya resim etrafında nasıl kaydırıldığını belirtir.

```cpp
enum class WrapType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 3 | Şekil etrafında metin sarma yok. Şekil, metnin arkasına veya önüne yerleştirilir. |
| Satır içi | 0 | Şekil, metinle aynı katmanda kalır ve bir karakter gibi işlenir. |
| TopBottom | 1 | Metin, şeklin üstünde durur ve şeklin altındaki satırda yeniden başlar. |
| Square | 2 | Metni, şeklin kare sınırlayıcı kutusunun tüm kenarları etrafında sarar. |
| Tight | 4 | Şeklin kenarları etrafında sıkı bir şekilde sarar, sınırlayıcı kutu etrafında sarmak yerine. |
| Through | 5 | Tight ile aynı, ancak şeklin açık olan bölümlerinin içine sarar. |


## Örnekler



Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görüntüyü başlığa ekleyin, böylece her sayfada görünür.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Görüntüyü sayfanın ortasına yerleştirin.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
