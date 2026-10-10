---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageBorderAppliesTo enum. Anger vilka sidor sidans kantlinje skrivs ut på i C++."
type: docs
weight: 106000
url: /sv/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Anger på vilka sidor sidramen skrivs ut.

```cpp
enum class PageBorderAppliesTo
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| AllPages | 0 | Sidkantlinjen visas på alla sidor i avsnittet. |
| FirstPage | 1 | Sidkantlinjen visas endast på den första sidan i avsnittet. |
| OtherPages | 2 | Sidkantlinjen visas på alla sidor förutom den första sidan i avsnittet. |


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
