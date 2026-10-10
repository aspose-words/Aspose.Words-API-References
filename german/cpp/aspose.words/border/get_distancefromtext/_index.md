---
title: "Aspose::Words::Border::get_DistanceFromText-Methode"
linktitle: "get_DistanceFromText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_DistanceFromText-Methode. Liest oder setzt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


Liest oder setzt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
