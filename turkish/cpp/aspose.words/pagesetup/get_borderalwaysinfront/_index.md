---
title: "Aspose::Words::PageSetup::get_BorderAlwaysInFront yöntemi"
linktitle: "get_BorderAlwaysInFront"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_BorderAlwaysInFront yöntemi. C++'ta sayfa kenarlığının kesişen metin ve nesnelere göre nerede konumlandırıldığını belirler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/pagesetup/get_borderalwaysinfront/
---
## PageSetup::get_BorderAlwaysInFront method


Sayfa kenarlığının kesişen metinler ve nesnelerle ilişkili konumunu belirtir.

```cpp
bool Aspose::Words::PageSetup::get_BorderAlwaysInFront()
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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
