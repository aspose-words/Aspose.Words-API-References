---
title: TableStyle.Alignment
second_title: Référence de l'API Aspose.Words pour .NET
description: TableStyle propriété. Spécifie lalignement du style de tableau.
type: docs
weight: 10
url: /fr/net/aspose.words/tablestyle/alignment/
---
## TableStyle.Alignment property

Spécifie l'alignement du style de tableau.

```csharp
public TableAlignment Alignment { get; set; }
```

### Remarques

La valeur par défaut estLeft .

### Exemples

Montre comment définir la position d'un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'aligner un tableau horizontalement.
// 1 - Utilisez la propriété "Alignement" pour l'aligner à un emplacement de la page, comme le centre :
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Insère un tableau et lui applique le style que nous avons créé.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Utilisez le "LeftIndent" pour spécifier un retrait à partir de la marge gauche de la page :
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### Voir également

* enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* class [TableStyle](../)
* espace de noms [Aspose.Words](../../tablestyle/)
* Assemblée [Aspose.Words](../../../)


