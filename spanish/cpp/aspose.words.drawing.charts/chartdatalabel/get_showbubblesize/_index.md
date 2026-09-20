---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize method"
linktitle: "get_ShowBubbleSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize method. Permite especificar si se mostrará el tamaño de la burbuja en las etiquetas de datos de un gráfico. Se aplica solo a gráficos de burbujas. El valor predeterminado es false en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabel/get_showbubblesize/
---
## ChartDataLabel::get_ShowBubbleSize method


Permite especificar si se debe mostrar el tamaño de la burbuja para las etiquetas de datos en un gráfico. Se aplica solo a los gráficos de burbujas. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize()
```


## Ejemplos



Muestra cómo usar efectos 3D con gráficos de burbujas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Aplica una etiqueta de datos a cada burbuja que muestre su diámetro.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## Ver también

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
