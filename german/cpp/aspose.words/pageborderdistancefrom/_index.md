---
title: "Aspose::Words::PageBorderDistanceFrom enum"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageBorderDistanceFrom enum. Gibt die Positionierung des Seitenrahmens relativ zum Seitenrand in C++ an."
type: docs
weight: 107000
url: /de/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


Gibt die Positionierung des Seitenrandes relativ zum Seitenrand an.

```cpp
enum class PageBorderDistanceFrom
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | 0 | Die Position von [Rand](../border/) wird vom Seitenrand gemessen. |
| PageEdge | 1 | Die Position von [Rand](../border/) wird von der Seitenkante gemessen. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
