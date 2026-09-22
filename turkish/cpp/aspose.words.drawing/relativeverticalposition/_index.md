---
title: "Aspose::Words::Drawing::RelativeVerticalPosition enum"
linktitle: "RelativeVerticalPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::RelativeVerticalPosition enum. Bir şeklin veya metin çerçevesinin dikey konumunun C++'da neye göre olduğunu belirtir."
type: docs
weight: 34000
url: /tr/cpp/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enum


Bir şeklin veya metin çerçevesinin dikey konumunun neye göre olduğunu belirtir.

```cpp
enum class RelativeVerticalPosition
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Kenar boşluğu | 0 | Dikey konumlandırmanın sayfa kenar boşluklarına göre olacağını belirtir. |
| Page | 1 | Nesne, sayfanın üst kenarına göre konumlandırılır. |
| Paragraph | 2 | Nesne, bağlantıyı içeren paragrafın üst kısmına göre konumlandırılır. |
| Çizgi | 3 | Belgelendirilmemiş. |
| TopMargin | 4 | Dikey konumlandırmanın geçerli sayfanın üst kenar boşluğuna göre olacağını belirtir. |
| BottomMargin | 5 | Dikey konumlandırmanın geçerli sayfanın alt kenar boşluğuna göre olacağını belirtir. |
| InsideMargin | 6 | Dikey konumlandırmanın geçerli sayfanın iç kenar boşluğuna göre olacağını belirtir. |
| OutsideMargin | 7 | Dikey konumlandırmanın geçerli sayfanın dış kenar boşluğuna göre olacağını belirtir. |
| TableDefault | n/a | Varsayılan değer [Margin](./) dir. |
| TextFrameDefault | n/a | Varsayılan değer [Paragraph](./). |


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
