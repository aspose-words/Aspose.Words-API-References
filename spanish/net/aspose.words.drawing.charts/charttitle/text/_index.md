---
title: ChartTitle.Text
second_title: Referencia de API de Aspose.Words para .NET
description: ChartTitle propiedad. Obtiene o establece el texto del título del gráfico. Sinulo o se especifica un valor vacío se mostrará el título generado automáticamente.
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Obtiene o establece el texto del título del gráfico. Si`nulo` o se especifica un valor vacío, se mostrará el título generado automáticamente.

```csharp
public string Text { get; set; }
```

### Observaciones

Usar[`Show`](../show/) opción si necesita ocultar el título.

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

* class [ChartTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../charttitle/)
* asamblea [Aspose.Words](../../../)


