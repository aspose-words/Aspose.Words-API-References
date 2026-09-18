---
title: "Aspose::Words::PageSetup::get_BorderAlwaysInFront‑Methode"
linktitle: "get_BorderAlwaysInFront"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_BorderAlwaysInFront‑Methode. Gibt an, wo der Seitenrand relativ zu überlappenden Texten und Objekten positioniert wird in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/pagesetup/get_borderalwaysinfront/
---
## PageSetup::get_BorderAlwaysInFront method


Gibt an, wo der Seitenrand relativ zu überlappenden Texten und Objekten positioniert ist.

```cpp
bool Aspose::Words::PageSetup::get_BorderAlwaysInFront()
```


## Beispiele



Zeigt, wie man einen breiten blauen Rahmen am oberen Rand der ersten Seite erstellt.
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

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
