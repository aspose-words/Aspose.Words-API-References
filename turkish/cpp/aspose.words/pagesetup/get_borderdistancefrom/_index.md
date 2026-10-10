---
title: "Aspose::Words::PageSetup::get_BorderDistanceFrom metodu"
linktitle: "get_BorderDistanceFrom"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_BorderDistanceFrom metodu. C++'ta belirtilen sayfa kenarlığının sayfa kenarından mı yoksa çevrelediği metinden mi ölçüldüğünü gösteren bir değeri alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/pagesetup/get_borderdistancefrom/
---
## PageSetup::get_BorderDistanceFrom method


Belirtilen sayfa kenarlığının sayfa kenarından mı yoksa çevresindeki metinden mi ölçüldüğünü gösteren bir değeri alır veya ayarlar.

```cpp
Aspose::Words::PageBorderDistanceFrom Aspose::Words::PageSetup::get_BorderDistanceFrom()
```


## Örnekler



İlk sayfanın üst kısmında geniş mavi şerit kenarlık oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## Ayrıca Bakınız

* Enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
