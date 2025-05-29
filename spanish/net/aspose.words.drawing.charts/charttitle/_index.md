---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartTitle para administrar y personalizar fácilmente los títulos de sus gráficos para una mejor visualización de datos.
type: docs
weight: 1140
url: /es/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Proporciona acceso a las propiedades del título del gráfico.

Para obtener más información, visite el[Trabajando con gráficos ](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartTitle
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | Proporciona acceso al formato de fuente del título del gráfico. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | Proporciona acceso al relleno y formato de línea del título del gráfico. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Determina si se permitirá que otros elementos del gráfico se superpongan al título. De forma predeterminada, la superposición es`FALSO` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Determina si se mostrará el título para este gráfico. El valor predeterminado es`verdadero` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Obtiene o establece el texto del título del gráfico. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente. |

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
