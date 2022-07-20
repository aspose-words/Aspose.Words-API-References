---
title: Show
second_title: Referencia de API de Aspose.Words para .NET
description: Determina si el título se mostrará para este gráfico. El valor predeterminado es verdadero.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Determina si el título se mostrará para este gráfico. El valor predeterminado es verdadero.

```csharp
public bool Show { get; set; }
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

* class [ChartTitle](../../charttitle)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../charttitle)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->