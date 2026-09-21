---
title: "Aspose::Words::PageSetup::get_BorderAlwaysInFront metod"
linktitle: "get_BorderAlwaysInFront"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_BorderAlwaysInFront metod. Anger var sidans ram placeras i förhållande till korsande texter och objekt i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/pagesetup/get_borderalwaysinfront/
---
## PageSetup::get_BorderAlwaysInFront method


Anger var sidramen är placerad i förhållande till korsande texter och objekt.

```cpp
bool Aspose::Words::PageSetup::get_BorderAlwaysInFront()
```


## Exempel



Visar hur man skapar en bred blå bandkant högst upp på den första sidan.
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

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
