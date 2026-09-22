---
title: "Aspose::Words::Border::get_Shadow metodu"
linktitle: "get_Shadow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border::get_Shadow metodu. C++'ta kenarın gölgeye sahip olup olmadığını gösteren bir değeri alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


Kenarın gölgesi olup olmadığını gösteren bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## Açıklamalar


Microsoft Word'de, bir kenarın gölgeye sahip olabilmesi için, dört tarafındaki (sol, üst, sağ ve alt) kenarlar aynı tür, genişlik, renk olmalı ve hepsinin Shadow özelliği **true** olarak ayarlanmış olmalıdır.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
