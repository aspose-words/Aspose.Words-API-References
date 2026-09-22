---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageBorderAppliesTo enum. Sayfa kenarlığının C++'da hangi sayfalara basıldığını belirtir."
type: docs
weight: 106000
url: /tr/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Sayfa kenarlığının hangi sayfalarda basılacağını belirtir.

```cpp
enum class PageBorderAppliesTo
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| AllPages | 0 | Sayfa kenarlığı, bölümün tüm sayfalarında gösterilir. |
| FirstPage | 1 | Sayfa kenarlığı yalnızca bölümün ilk sayfasında gösterilir. |
| OtherPages | 2 | Sayfa kenarlığı, bölümün ilk sayfası dışındaki tüm sayfalarda gösterilir. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
