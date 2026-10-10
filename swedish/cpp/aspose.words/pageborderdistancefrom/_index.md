---
title: "Aspose::Words::PageBorderDistanceFrom enum"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageBorderDistanceFrom enum. Anger placeringen av sidans kantlinje i förhållande till sidmarginalen i C++."
type: docs
weight: 107000
url: /sv/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


Anger placeringen av sidramen i förhållande till sidmarginalen.

```cpp
enum class PageBorderDistanceFrom
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | 0 | Placeringen av [Border](../border/) mäts från sidmarginalen. |
| PageEdge | 1 | Placeringen av [Border](../border/) mäts från sidans kant. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
