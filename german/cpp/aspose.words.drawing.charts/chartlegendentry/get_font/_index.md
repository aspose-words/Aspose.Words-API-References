---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font Methode"
linktitle: "get_Font"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font Methode. Bietet Zugriff auf die Schriftformatierung dieses Legendeeintrags in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing.charts/chartlegendentry/get_font/
---
## ChartLegendEntry::get_Font method


Stellt Zugriff auf die Schriftformatierung dieses Legendeeintrags bereit.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font()
```


## Beispiele



Zeigt, wie man mit einer Legenden‑Schriftart arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Standard‑Schriftgröße für alle Legendeeinträge festlegen.
chartLegend->get_Font()->set_Size(14);
// Schriftart für einen bestimmten Legendeeintrag ändern.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Legendeeintrag für Diagrammreihe abrufen.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Siehe auch

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegendEntry](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
