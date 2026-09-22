---
title: "Aspose::Words::BorderCollection::get_LineWidth metodu"
linktitle: "get_LineWidth"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::get_LineWidth metodu. C++'ta kenar genişliğini puan cinsinden alır veya ayarlar."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/bordercollection/get_linewidth/
---
## BorderCollection::get_LineWidth method


Kenar genişliğini puan cinsinden alır veya ayarlar.

```cpp
double Aspose::Words::BorderCollection::get_LineWidth()
```

## Açıklamalar


Koleksiyondaki ilk kenarın genişliğini döndürür.

Koleksiyondaki tüm kenarların genişliğini, çapraz kenarlar hariç, ayarlar.

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
