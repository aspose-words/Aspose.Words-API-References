---
title: ChartTitle.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartTitle Overlay, que permite superponer elementos de control para una visualización más clara. ¡Mejore sus gráficos fácilmente con esta sencilla configuración!
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

Determina si se permitirá que otros elementos del gráfico se superpongan al título. De forma predeterminada, la superposición es`FALSO` .

```csharp
public bool Overlay { get; set; }
```

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

* class [ChartTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
