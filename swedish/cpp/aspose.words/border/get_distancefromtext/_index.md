---
title: "Aspose::Words::Border::get_DistanceFromText‑metod"
linktitle: "get_DistanceFromText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Border::get_DistanceFromText‑metod. Hämtar eller anger avståndet för kanten från texten eller från sidans kant i punkter i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


Hämtar eller anger avståndet för kanten från texten eller från sidans kant i punkter.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
