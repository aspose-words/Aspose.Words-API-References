---
title: ChartTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: ¡Personaliza el título de tu gráfico fácilmente! Configura u obtén la propiedad ChartTitle Text para un toque personalizado. Genera títulos automáticamente cuando los necesites.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Obtiene o establece el texto del título del gráfico. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente.

```csharp
public string Text { get; set; }
```

## Observaciones

Usar[`Show`](../show/) Opción si necesita ocultar el título.

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
