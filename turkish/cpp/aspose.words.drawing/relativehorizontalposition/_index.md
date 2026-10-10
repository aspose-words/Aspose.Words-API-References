---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. C++'de bir şeklin veya metin çerçevesinin yatay konumunun neye göre belirlendiğini belirtir."
type: docs
weight: 33000
url: /tr/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


Bir şeklin veya metin çerçevesinin yatay konumunun neye göre olduğunu belirtir.

```cpp
enum class RelativeHorizontalPosition
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Kenar boşluğu | 0 | Yatay konumlamanın sayfa kenar boşluklarına göre olacağını belirtir. |
| Page | 1 | Nesne, sayfanın sol kenarına göre konumlandırılır. |
| Sütun | 2 | Nesne, sütunun sol tarafına göre konumlandırılır. |
| Character | 3 | Nesne, paragrafın sol tarafına göre konumlandırılır. |
| LeftMargin | 4 | Yatay konumlamanın sayfanın sol kenar boşluğuna göre olacağını belirtir. |
| RightMargin | 5 | Yatay konumlamanın sayfanın sağ kenar boşluğuna göre olacağını belirtir. |
| InsideMargin | 6 | Yatay konumlamanın geçerli sayfanın iç kenar boşluğuna göre olacağını belirtir (tek sayfalarda sol kenar boşluğu, çift sayfalarda sağ kenar boşluğu). |
| OutsideMargin | 7 | Yatay konumlamanın geçerli sayfanın dış kenar boşluğuna göre olacağını belirtir (tek sayfalarda sağ kenar boşluğu, çift sayfalarda sol kenar boşluğu). |
| Default | n/a | Varsayılan değer [Column](./). |


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
