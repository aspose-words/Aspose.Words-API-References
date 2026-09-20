---
title: "Método Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat"
linktitle: "HasDefaultFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat. Obtiene una bandera que indica si el punto de datos en el índice especificado tiene formato predeterminado en C++."
type: docs
weight: 5500
url: /es/cpp/aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/
---
## ChartDataPointCollection::HasDefaultFormat method


Obtiene una bandera que indica si el punto de datos en el índice especificado tiene el formato predeterminado.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat(int32_t dataPointIndex)
```


## Ejemplos



Mostrar cómo copiar el formato del punto de datos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Obtener el gráfico y la serie para actualizar el formato.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// Copiar el formato del punto de datos con índice 1 al punto de datos con índice 2
// para que el punto de datos 2 se vea igual que el punto de datos 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Copiar el formato del punto de datos con índice 0 a los valores predeterminados de la serie para que todos los puntos de datos
// en la serie que tiene el formato predeterminado, se ve igual que el punto de datos 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## Ver también

* Class [ChartDataPointCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
