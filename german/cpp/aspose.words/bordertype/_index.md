---
title: "Aspose::Words::BorderType Aufzählung"
linktitle: "BorderType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderType Aufzählung. Gibt die Seiten eines Rahmens an. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 81000
url: /de/cpp/aspose.words/bordertype/
---
## BorderType enum


Gibt die Seiten eines Rahmens an. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
enum class BorderType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | -1 | Standardwert. |
| Unten | 0 | Gibt den unteren Rand eines Absatzes oder einer Tabellenzelle an. |
| Links | 1 | Gibt den linken Rand eines Absatzes oder einer Tabellenzelle an. |
| Rechts | 2 | Gibt den rechten Rand eines Absatzes oder einer Tabellenzelle an. |
| Oben | 3 | Gibt den oberen Rand eines Absatzes oder einer Tabellenzelle an. |
| Horizontal | 4 | Gibt den horizontalen Rand zwischen Zellen in einer Tabelle oder zwischen zusammengehörigen Absätzen an. |
| Vertikal | 5 | Gibt den vertikalen Rand zwischen Zellen in einer Tabelle an. |
| DiagonalDown | 6 | Gibt den diagonalen Rand in einer Tabellenzelle an. |
| DiagonalUp | 7 | Gibt den diagonalen Rand in einer Tabellenzelle an. |


## Beispiele



Zeigt, wie man einen Absatz mit einem oberen Rand einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Setze ThemeColor nur, wenn LineWidth oder LineStyle gesetzt ist.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
