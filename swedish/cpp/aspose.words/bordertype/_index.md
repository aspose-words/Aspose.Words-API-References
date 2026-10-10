---
title: "Aspose::Words::BorderType enum"
linktitle: "BorderType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BorderType‑enum. Anger sidorna på en ram. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 81000
url: /sv/cpp/aspose.words/bordertype/
---
## BorderType enum


Anger sidorna på en ram. För att lära dig mer, besök artikeln [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) i dokumentationen.

```cpp
enum class BorderType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | -1 | Standardvärde. |
| Bottom | 0 | Anger den nedre kanten av ett stycke eller en tabellcell. |
| Vänster | 1 | Anger den vänstra kanten av ett stycke eller en tabellcell. |
| Höger | 2 | Anger den högra kanten av ett stycke eller en tabellcell. |
| Top | 3 | Anger den övre kanten av ett stycke eller en tabellcell. |
| Horisontell | 4 | Anger den horisontella kanten mellan celler i en tabell eller mellan motsvarande stycken. |
| Vertikal | 5 | Anger den vertikala kanten mellan celler i en tabell. |
| DiagonalDown | 6 | Anger den diagonala kanten i en tabellcell. |
| DiagonalUp | 7 | Anger den diagonala kanten i en tabellcell. |


## Exempel



Visar hur man infogar ett stycke med en övre kant.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Ställ in ThemeColor endast när LineWidth eller LineStyle har satts.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
