---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words para .NET
description: Desbloquee potentes propiedades de formas de gráficos con la clase Aspose.Words.Drawing.Charts.Chart. Mejore sus documentos con una representación visual dinámica de datos.
type: docs
weight: 880
url: /es/net/aspose.words.drawing.charts/chart/
---
## Chart class

Proporciona acceso a las propiedades de forma del gráfico.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class Chart
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Obtiene una colección de todos los ejes de este gráfico. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Proporciona acceso a las propiedades del eje X principal del gráfico. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Proporciona acceso a las propiedades del eje Y principal del gráfico. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Proporciona acceso a las propiedades del eje Z del gráfico. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Proporciona acceso a las propiedades de una tabla de datos de este gráfico. La tabla de datos se puede mostrar utilizando el[`Show`](../chartdatatable/show/) propiedad. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Proporciona acceso al relleno y formato de línea del gráfico. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Proporciona acceso a las propiedades de la leyenda del gráfico. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Proporciona acceso a la colección de series. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Proporciona acceso a una colección de grupos de series de este gráfico. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Obtiene la ruta y el nombre de un archivo xls/xlsx al que está vinculado este gráfico. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Obtiene o establece el estilo del gráfico. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Proporciona acceso a las propiedades del título del gráfico. |

## Ejemplos

Muestra cómo insertar un gráfico y establecer un título.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una forma de gráfico con un generador de documentos y obtenga su gráfico.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Utilice la propiedad "Título" para darle un título a nuestro gráfico, que aparece en la parte superior central del área del gráfico.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // Establezca la propiedad "Mostrar" en "verdadero" para que el título sea visible.
title.Show = true;

// Establezca la propiedad "Superposición" en "verdadero". Otorgue más espacio a otros elementos del gráfico permitiéndoles superponerse al título.
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
