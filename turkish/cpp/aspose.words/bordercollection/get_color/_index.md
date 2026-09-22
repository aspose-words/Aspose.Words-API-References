---
title: "Aspose::Words::BorderCollection::get_Color metodu"
linktitle: "get_Color"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::get_Color metodu. C++'ta kenar rengini alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


Kenar rengini alır veya ayarlar.

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## Açıklamalar


Koleksiyondaki ilk kenarın rengini döndürür.

Koleksiyondaki tüm kenarların rengini, çapraz kenarlar hariç, ayarlar.

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
