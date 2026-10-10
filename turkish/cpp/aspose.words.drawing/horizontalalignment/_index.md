---
title: "Aspose::Words::Drawing::HorizontalAlignment enum"
linktitle: "HorizontalAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::HorizontalAlignment enum. Yüzen bir şeklin, metin çerçevesinin veya yüzen bir tablonun C++'deki yatay hizalamasını belirtir."
type: docs
weight: 26000
url: /tr/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Yüzen bir şekil, metin çerçevesi veya yüzen tablo için yatay hizalamayı belirtir.

```cpp
enum class HorizontalAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Nesne açıkça konumlandırılır, genellikle **Left** özelliği kullanılarak. |
| Default | n/a | Aynı [None](./) ile. |
| Sol | 1 | Nesnenin yatay hizalama tabanına sola hizalanacağını belirtir. |
| Orta | 2 | Nesnenin yatay hizalama tabanına göre ortalanacağını belirtir. |
| Sağ | 3 | Nesnenin yatay hizalama temeline sağa hizalanacağını belirtir. |
| İçinde | 4 | Nesnenin yatay hizalama tabanının içinde olacağını belirtir. |
| Dış | 5 | Nesnenin yatay hizalama temelinin dışına yerleştirileceğini belirtir. |


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
