---
title: "Aspose::Words::BorderCollection::get_LineStyle yöntemi"
linktitle: "get_LineStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::get_LineStyle yöntemi. C++'da kenarlık stilini alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


Kenar stilini alır veya ayarlar.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## Açıklamalar


Koleksiyondaki ilk kenarlığın stilini döndürür.

Koleksiyondaki tüm kenarlıkların stilini, diyagonal kenarlıklar hariç, ayarlar.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
