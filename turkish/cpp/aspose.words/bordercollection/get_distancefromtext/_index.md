---
title: "Aspose::Words::BorderCollection::get_DistanceFromText method"
linktitle: "get_DistanceFromText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::get_DistanceFromText method. C++'ta kenarlığın metinden uzaklığını nokta cinsinden alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Kenarın metinden puan cinsinden uzaklığını alır veya ayarlar.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Açıklamalar


İlk kenarlık için metinden uzaklığı alır.

Koleksiyondaki tüm kenarlar için, çapraz kenarlar hariç, metinden olan mesafeyi ayarlar.

Etki yapmaz ve tablo hücrelerinin kenarları için otomatik olarak sıfıra sıfırlanır.

## Örnekler



Gölge ile yeşil dalgalı sayfa kenarı oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## Ayrıca Bakınız

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
