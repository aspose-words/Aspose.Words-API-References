---
title: "Aspose::Words::PageSetup::get_BorderAppliesTo metod"
linktitle: "get_BorderAppliesTo"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_BorderAppliesTo metod. Anger vilka sidor sidans ram skrivs ut på i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/pagesetup/get_borderappliesto/
---
## PageSetup::get_BorderAppliesTo method


Anger på vilka sidor sidramen skrivs ut.

```cpp
Aspose::Words::PageBorderAppliesTo Aspose::Words::PageSetup::get_BorderAppliesTo()
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

* Enum [PageBorderAppliesTo](../../pageborderappliesto/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
