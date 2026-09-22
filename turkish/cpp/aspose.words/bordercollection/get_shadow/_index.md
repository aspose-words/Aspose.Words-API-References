---
title: "Aspose::Words::BorderCollection::get_Shadow metodu"
linktitle: "get_Shadow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::get_Shadow metodu. C++'ta kenarın gölgeye sahip olup olmadığını belirten bir değeri alır veya ayarlar."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


Kenarın gölgesi olup olmadığını gösteren bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## Açıklamalar


Koleksiyondaki ilk kenardan değeri alır.

Koleksiyondaki tüm kenarlar için, çapraz kenarlar hariç, değeri ayarlar.

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
