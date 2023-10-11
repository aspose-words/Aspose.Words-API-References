---
title: Chart.SourceFullName
second_title: Aspose.Words per .NET API Reference
description: Chart proprietà. Ottiene il percorso e il nome di un file xls/xlsx a cui è collegato questo grafico.
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Ottiene il percorso e il nome di un file xls/xlsx a cui è collegato questo grafico.

```csharp
public string SourceFullName { get; set; }
```

### Esempi

Mostra come ottenere/impostare il nome completo del documento xls/xlsx esterno se il grafico è collegato.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));

sourceFullName = "D:\\Documents\\ChartData.xlsx";
Assert.True(sourceFullName.Equals("D:\\Documents\\ChartData.xlsx", StringComparison.Ordinal));
```

### Guarda anche

* class [Chart](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chart/)
* assemblea [Aspose.Words](../../../)


