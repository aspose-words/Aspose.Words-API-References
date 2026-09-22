---
title: "Aspose::Words::Drawing::VerticalAlignment enum"
linktitle: "VerticalAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::VerticalAlignment enum. Yüzen bir şeklin, metin çerçevesinin veya yüzen bir tablonun dikey hizalamasını C++'da belirtir."
type: docs
weight: 43000
url: /tr/cpp/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enum


Kayan bir şekil, metin çerçevesi veya kayan bir tablo için dikey hizalamayı belirtir.

```cpp
enum class VerticalAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Nesne açıkça konumlandırılmıştır, genellikle **Top** özelliği kullanılarak. |
| Üst | 1 | Nesnenin dikey hizalama tabanının üstünde olacağını belirtir. |
| Orta | 2 | Nesnenin dikey hizalama tabanına göre ortalanacağını belirtir. |
| Alt | 3 | Nesnenin dikey hizalama tabanının altında olacağını belirtir. |
| İçinde | 4 | Nesnenin yatay hizalama tabanının içinde olacağını belirtir. |
| Dış | 5 | Nesnenin dikey hizalama tabanının dışında olacağını belirtir. |
| Satır içi | -1 | Belgelendirilmemiştir. Yüzen paragraflar ve tablolar için olası bir değer gibi görünüyor. |
| Default | n/a | Aynı [None](./) ile. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
