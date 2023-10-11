---
title: Chart.SourceFullName
second_title: Aspose.Words für .NET-API-Referenz
description: Chart eigendom. Ruft den Pfad und Namen einer XLS/XLSXDatei ab mit der dieses Diagramm verknüpft ist.
type: docs
weight: 70
url: /de/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Ruft den Pfad und Namen einer XLS/XLSX-Datei ab, mit der dieses Diagramm verknüpft ist.

```csharp
public string SourceFullName { get; set; }
```

### Beispiele

Zeigt, wie der vollständige Name des externen XLS/XLSX-Dokuments abgerufen/festgelegt wird, wenn das Diagramm verknüpft ist.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));

sourceFullName = "D:\\Documents\\ChartData.xlsx";
Assert.True(sourceFullName.Equals("D:\\Documents\\ChartData.xlsx", StringComparison.Ordinal));
```

### Siehe auch

* class [Chart](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chart/)
* Montage [Aspose.Words](../../../)


