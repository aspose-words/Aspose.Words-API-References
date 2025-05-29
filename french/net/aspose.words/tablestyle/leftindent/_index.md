---
title: TableStyle.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TableStyle LeftIndent pour personnaliser facilement le retrait à gauche de votre tableau pour un contrôle de mise en page amélioré et un attrait visuel.
type: docs
weight: 90
url: /fr/net/aspose.words/tablestyle/leftindent/
---
## TableStyle.LeftIndent property

Obtient ou définit la valeur qui représente le retrait à gauche d'un tableau.

```csharp
public double LeftIndent { get; set; }
```

## Exemples

Montre comment définir la position d'un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux manières d'aligner un tableau horizontalement.
// 1 - Utilisez la propriété « Alignment » pour l'aligner sur un emplacement de la page, comme le centre :
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Insérez un tableau et appliquez-lui le style que nous avons créé.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Utilisez « LeftIndent » pour spécifier un retrait à partir de la marge gauche de la page :
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

* class [TableStyle](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
