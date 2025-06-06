---
title: ChartTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words para .NET
description: Mejore sus gráficos con títulos personalizables. Controle la visibilidad fácilmente (valor predeterminado "true"). ¡Mejore la presentación de sus datos hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Determina si se mostrará el título para este gráfico. El valor predeterminado es`verdadero` .

```csharp
public bool Show { get; set; }
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
