---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words pour .NET
description: Chart SourceFullName propriété. Obtient le chemin et le nom dun fichier xls/xlsx auquel ce graphique est lié en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Obtient le chemin et le nom d'un fichier xls/xlsx auquel ce graphique est lié.

```csharp
public string SourceFullName { get; set; }
```

## Exemples

Montre comment obtenir/définir le nom complet du document xls/xlsx externe si le graphique est lié.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));

sourceFullName = "D:\\Documents\\ChartData.xlsx";
Assert.True(sourceFullName.Equals("D:\\Documents\\ChartData.xlsx", StringComparison.Ordinal));
```

### Voir également

* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
