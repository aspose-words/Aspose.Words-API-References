---
title: "Aspose::Words::Border::get_DistanceFromText yöntemi"
linktitle: "get_DistanceFromText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border::get_DistanceFromText yöntemi. C++'ta kenarın metinden veya sayfa kenarından nokta cinsinden uzaklığını alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


Kenarlığın metinden veya sayfa kenarından puan cinsinden uzaklığını alır veya ayarlar.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
