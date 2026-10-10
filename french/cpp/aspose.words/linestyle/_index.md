---
title: "Aspose::Words::LineStyle enum"
linktitle: "LineStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LineStyle enum. Spécifie le style de ligne d'une Border en C++."
type: docs
weight: 96000
url: /fr/cpp/aspose.words/linestyle/
---
## LineStyle enum


Spécifie le style de ligne d'une [Border](../border/).

```cpp
enum class LineStyle
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 |  |
| Simple | 1 |  |
| Épais | 2 |  |
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
| Wave | 20 |  |
| DoubleWave | 21 |  |
| DashSmallGap | 22 |  |
| DashDotStroker | 23 |  |
| Emboss3D | 24 |  |
| Engrave3D | 25 |  |
| Outset | 26 |  |
| Inset | 27 |  |


## Exemples



Montre comment insérer une chaîne entourée d'une bordure dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
