---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Chart SourceFullName“, um einfach auf den Pfad und den Namen verknüpfter XLS/XLSX-Dateien zuzugreifen und so die Datenvisualisierung zu verbessern.
type: docs
weight: 100
url: /de/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Ruft den Pfad und Namen einer XLS-/XLSX-Datei ab, mit der dieses Diagramm verknüpft ist.

```csharp
public string SourceFullName { get; set; }
```

## Beispiele

Zeigt, wie der vollständige Name des externen XLS-/XLSX-Dokuments abgerufen/festgelegt wird, wenn das Diagramm verknüpft ist.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### Siehe auch

* class [Chart](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
