---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories Methode"
linktitle: "get_AxisBetweenCategories"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories Methode. Gibt ein Flag zurück oder setzt es, das angibt, ob die Werteachse die Kategorienachse zwischen den Kategorien in C++ schneidet."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing.charts/chartaxis/get_axisbetweencategories/
---
## ChartAxis::get_AxisBetweenCategories method


Ermittelt oder legt ein Flag fest, das angibt, ob die Werteachse die Kategorienachse zwischen den Kategorien schneidet.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories()
```


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
