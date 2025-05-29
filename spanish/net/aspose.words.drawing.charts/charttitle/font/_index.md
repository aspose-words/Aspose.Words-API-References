---
title: ChartTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words para .NET
description: Personaliza el título de tu gráfico con la propiedad Fuente ChartTitle para un formato de fuente mejorado. ¡Mejora la presentación de tus datos sin esfuerzo!
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/charttitle/font/
---
## ChartTitle.Font property

Proporciona acceso al formato de fuente del título del gráfico.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
