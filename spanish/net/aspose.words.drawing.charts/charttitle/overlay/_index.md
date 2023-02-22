---
title: ChartTitle.Overlay
second_title: Referencia de API de Aspose.Words para .NET
description: ChartTitle propiedad. Determina si se permitirá que otros elementos del gráfico se superpongan al título. Por defecto la superposición es falsa.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

Determina si se permitirá que otros elementos del gráfico se superpongan al título. Por defecto, la superposición es falsa.

```csharp
public bool Overlay { get; set; }
```

### Ejemplos

Muestra cómo insertar un gráfico y establecer un título.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una forma de gráfico con un generador de documentos y obtenga su gráfico.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Use la propiedad "Título" para darle un título a nuestro gráfico, que aparece en la parte superior central del área del gráfico.
ChartTitle title = chart.Title;
title.Text = "My Chart";

  // Establezca la propiedad "Mostrar" en "verdadero" para que el título sea visible.
title.Show = true;

// Establezca la propiedad "Superposición" en "verdadero" Dé más espacio a otros elementos del gráfico permitiéndoles superponerse al título
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Ver también

* class [ChartTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../charttitle/)
* asamblea [Aspose.Words](../../../)


