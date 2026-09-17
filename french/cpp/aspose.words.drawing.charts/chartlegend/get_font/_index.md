---
title: "Aspose::Words::Drawing::Charts::ChartLegend::get_Font méthode"
linktitle: "get_Font"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend::get_Font méthode. Fournit l'accès au formatage de police par défaut des entrées de légende. Pour remplacer le formatage de police d'une entrée de légende spécifique, utilisez la propriété theFont en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing.charts/chartlegend/get_font/
---
## ChartLegend::get_Font method


Fournit l'accès au formatage de police par défaut des entrées de légende. Pour remplacer le formatage de police d'une entrée de légende spécifique, utilisez la propriété [Font](../../chartlegendentry/get_font/).

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegend::get_Font()
```


## Exemples



Montre comment travailler avec une police de légende.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Définir la taille de police par défaut pour toutes les entrées de légende.
chartLegend->get_Font()->set_Size(14);
// Modifier la police d'une entrée de légende spécifique.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Obtenir l'entrée de légende pour une série de graphique.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Voir aussi

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
