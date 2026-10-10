---
title: "Aspose::Words::LineStyle enum"
linktitle: "LineStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LineStyle enum. Anger linjestil för en Border i C++."
type: docs
weight: 96000
url: /sv/cpp/aspose.words/linestyle/
---
## LineStyle enum


Anger linjestil för en [Border](../border/).

```cpp
enum class LineStyle
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 |  |
| Enkel | 1 |  |
| Tjock | 2 |  |
| Dubbel | 3 |  |
| Hairline | 5 |  |
| Dot | 6 |  |
| DashLargeGap | 7 |  |
| Punktstreck | 8 |  |
| Punktpunktstreck | 9 |  |
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
| Våg | 20 |  |
| DubbelVåg | 21 |  |
| StreckLitetMellanrum | 22 |  |
| StreckPunktStrokare | 23 |  |
| Emboss3D | 24 |  |
| Engrave3D | 25 |  |
| Utgång | 26 |  |
| Inskjutning | 27 |  |


## Exempel



Visar hur man infogar en sträng omgiven av en kant i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
