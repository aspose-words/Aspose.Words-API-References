---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories metodo"
linktitle: "get_AxisBetweenCategories"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories metodo. Ottiene o imposta un flag che indica se l'asse dei valori attraversa l'asse delle categorie tra le categorie in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing.charts/chartaxis/get_axisbetweencategories/
---
## ChartAxis::get_AxisBetweenCategories method


Ottiene o imposta un flag che indica se l'asse dei valori attraversa l'asse delle categorie tra le categorie.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories()
```


## Esempi



Mostra come far attraversare un asse del grafico a una posizione personalizzata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Per i grafici a colonne, l'asse Y attraversa lo zero per impostazione predefinita,
// il che significa che le colonne per tutti i valori inferiori a zero puntano verso il basso per rappresentare i valori negativi.
// Possiamo impostare un valore diverso per l'intersezione dell'asse Y. In questo caso, lo imposteremo a 3.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## Vedi anche

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
