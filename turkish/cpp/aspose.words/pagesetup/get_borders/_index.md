---
title: "Aspose::Words::PageSetup::get_Borders metodu"
linktitle: "get_Borders"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_Borders metodu. C++'ta sayfa kenarlıklarının bir koleksiyonunu alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/pagesetup/get_borders/
---
## PageSetup::get_Borders method


Sayfa kenarlıklarının bir koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::PageSetup::get_Borders()
```


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

* Class [BorderCollection](../../bordercollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
