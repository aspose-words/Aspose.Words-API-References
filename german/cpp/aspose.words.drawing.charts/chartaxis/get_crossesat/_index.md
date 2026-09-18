---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt Methode"
linktitle: "get_CrossesAt"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt-Methode. Gibt an, wo auf der senkrechten Achse die Achse in C++ schneidet."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/chartaxis/get_crossesat/
---
## ChartAxis::get_CrossesAt method


Gibt an, wo auf der senkrechten Achse die Achse schneidet.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt()
```

## Hinweise


Die Eigenschaft wirkt nur, wenn [Crosses](../get_crosses/) auf [Custom](../../axiscrosses/) gesetzt ist. Sie wird von den neuen Diagrammen in MS Office 2016 nicht unterstützt.

Die Einheiten werden durch den Achsentyp bestimmt. Ist die Achse eine Werteachse, ist der Wert der Eigenschaft eine Dezimalzahl auf der Werteachse. Ist die Achse eine Zeitkategorie‑Achse, wird der Wert als ganze Zahl von Tagen relativ zum Basisdatum (30/12/1899) definiert. Für eine Text‑Kategorie‑Achse ist der Wert eine ganzzahlige Kategorienummer, beginnend mit 1 als erste Kategorie.

## Beispiele



Zeigt, wie man eine Diagrammachse an einer benutzerdefinierten Position kreuzen lässt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Bei Säulendiagrammen schneidet die Y‑Achse standardmäßig bei Null,
// was bedeutet, dass Säulen für alle Werte unter Null nach unten zeigen, um negative Werte darzustellen.
// Wir können einen anderen Wert für den Y‑Achsen‑Schnittpunkt festlegen. In diesem Fall setzen wir ihn auf 3.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## Siehe auch

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
