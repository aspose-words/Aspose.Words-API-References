---
title: "Aspose::Words::LineStyle Enum"
linktitle: "LineStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LineStyle Enum. Gibt den Linienstil eines Borders in C++ an."
type: docs
weight: 96000
url: /de/cpp/aspose.words/linestyle/
---
## LineStyle enum


Gibt den Linienstil eines [Border](../border/) an.

```cpp
enum class LineStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 |  |
| Single | 1 |  |
| Thick | 2 |  |
| Double | 3 |  |
| Hairline | 5 |  |
| Dot | 6 |  |
| DashLargeGap | 7 |  |
| DotDash | 8 |  |
| DotDotDash | 9 |  |
| Triple | 10 |  |
| ThinThickSmallGap | 11 |  |
| ThickThinSmallGap | 12 |  |
| ThinThickThinSmallGap | 13 |  |
| ThinThickMediumGap | 14 |  |
| ThickThinMediumGap | 15 |  |
| ThinThickThinMediumGap | 16 |  |
| ThinThickLargeGap | 17 |  |
| ThickThinLargeGap | 18 |  |
| ThinThickThinLargeGap | 19 |  |
| Welle | 20 |  |
| DoppelteWelle | 21 |  |
| StrichKleineLücke | 22 |  |
| StrichPunktStreicher | 23 |  |
| Prägen3D | 24 |  |
| Gravieren3D | 25 |  |
| Außen | 26 |  |
| Innen | 27 |  |


## Beispiele



Zeigt, wie man eine von einem Rahmen umgebene Zeichenkette in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
