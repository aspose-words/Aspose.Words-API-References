---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Chart SourceFullName pour accéder facilement au chemin et au nom des fichiers XLS/XLSX liés pour une visualisation améliorée des données.
type: docs
weight: 100
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
```

### Voir également

* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
