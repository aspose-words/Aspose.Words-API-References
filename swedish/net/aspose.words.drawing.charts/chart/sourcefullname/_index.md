---
title: Chart.SourceFullName
second_title: Aspose.Words för .NET API Referens
description: Chart fast egendom. Hämtar sökvägen och namnet på en xls/xlsxfil som detta diagram är länkat till.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Hämtar sökvägen och namnet på en xls/xlsx-fil som detta diagram är länkat till.

```csharp
public string SourceFullName { get; set; }
```

### Exempel

Visar hur man får det fullständiga namnet på det externa xls/xlsx-dokumentet om diagrammet är länkat.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.True(shape.Chart.SourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### Se även

* class [Chart](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chart/)
* hopsättning [Aspose.Words](../../../)


