---
title: Chart.SourceFullName
second_title: Referencia de API de Aspose.Words para .NET
description: Chart propiedad. Obtiene la ruta y el nombre de un archivo xls/xlsx al que está vinculado este gráfico.
type: docs
weight: 70
url: /es/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Obtiene la ruta y el nombre de un archivo xls/xlsx al que está vinculado este gráfico.

```csharp
public string SourceFullName { get; set; }
```

### Ejemplos

Muestra cómo obtener/establecer el nombre completo del documento xls/xlsx externo si el gráfico está vinculado.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));

sourceFullName = "D:\\Documents\\ChartData.xlsx";
Assert.True(sourceFullName.Equals("D:\\Documents\\ChartData.xlsx", StringComparison.Ordinal));
```

### Ver también

* class [Chart](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chart/)
* asamblea [Aspose.Words](../../../)


