---
title: Class ChartTitle
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartTitle clase. Proporciona acceso a las propiedades del título del gráfico.
type: docs
weight: 820
url: /es/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Proporciona acceso a las propiedades del título del gráfico.

Para obtener más información, visite el[Trabajar con gráficos ](https://docs.aspose.com/words/net/working-with-charts/) artículo de documentación.

```csharp
public class ChartTitle
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } |  |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Determina si se permitirá que otros elementos del gráfico se superpongan al título. De forma predeterminada, la superposición es`FALSO` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Determina si el título se mostrará para este gráfico. El valor predeterminado es`verdadero` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Obtiene o establece el texto del título del gráfico. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente. |

### Ejemplos

Muestra cómo insertar un gráfico y establecer un título.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una forma de gráfico con un generador de documentos y obtén su gráfico.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Utilice la propiedad "Título" para darle un título a nuestro gráfico, que aparece en la parte superior central del área del gráfico.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Establece la propiedad "Mostrar" en "verdadero" para que el título sea visible.
title.Show = true;

// Establece la propiedad "Superposición" en "verdadero" Da más espacio a otros elementos del gráfico permitiéndoles superponerse al título
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)


