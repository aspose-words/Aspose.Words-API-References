---
title: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat metodo"
linktitle: "HasDefaultFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat metodo. Ottiene un flag che indica se il punto dati all'indice specificato ha il formato predefinito in C++."
type: docs
weight: 5500
url: /it/cpp/aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/
---
## ChartDataPointCollection::HasDefaultFormat method


Ottiene un flag che indica se il punto dati all'indice specificato ha il formato predefinito.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat(int32_t dataPointIndex)
```


## Esempi



Mostra come copiare il formato del punto dati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Ottieni il grafico e la serie per aggiornare il formato.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// Copia il formato del punto dati con indice 1 al punto dati con indice 2
// in modo che il punto dati 2 abbia lo stesso aspetto del punto dati 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Copia il formato del punto dati con indice 0 nelle impostazioni predefinite della serie in modo che tutti i punti dati
// nella serie che hanno il formato predefinito appaiono uguali al punto dati 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## Vedi anche

* Class [ChartDataPointCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
