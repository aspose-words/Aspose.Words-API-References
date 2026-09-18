---
title: "Aspose::Words::PageBorderAppliesTo Enum"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageBorderAppliesTo Enum. Gibt an, auf welchen Seiten der Seitenrand in C++ gedruckt wird."
type: docs
weight: 106000
url: /de/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Gibt an, auf welchen Seiten der Seitenrand gedruckt wird.

```cpp
enum class PageBorderAppliesTo
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AllPages | 0 | Der Seitenrand wird auf allen Seiten des Abschnitts angezeigt. |
| FirstPage | 1 | Der Seitenrand wird nur auf der ersten Seite des Abschnitts angezeigt. |
| OtherPages | 2 | Der Seitenrand wird auf allen Seiten außer der ersten Seite des Abschnitts angezeigt. |


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
