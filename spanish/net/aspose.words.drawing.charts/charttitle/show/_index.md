---
title: ChartTitle.Show
second_title: Referencia de API de Aspose.Words para .NET
description: ChartTitle propiedad. Determina si el título se mostrará para este gráfico. El valor predeterminado esverdadero .
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Determina si el título se mostrará para este gráfico. El valor predeterminado es`verdadero` .

```csharp
public bool Show { get; set; }
```

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


