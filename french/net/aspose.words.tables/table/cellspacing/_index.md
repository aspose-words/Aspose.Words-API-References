---
title: Table.CellSpacing
second_title: Référence de l'API Aspose.Words pour .NET
description: Table propriété. Obtient ou définit la quantité despace en points entre les cellules.
type: docs
weight: 100
url: /fr/net/aspose.words.tables/table/cellspacing/
---
## Table.CellSpacing property

Obtient ou définit la quantité d'espace (en points) entre les cellules.

```csharp
public double CellSpacing { get; set; }
```

### Exemples

Montre comment activer l’espacement entre les cellules individuelles d’un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Définissez la propriété "AllowCellSpacing" sur "true" pour activer l'espacement entre les cellules
// d'une grandeur égale à la valeur de la propriété "CellSpacing", en points.
// Définissez la propriété "AllowCellSpacing" sur "false" pour désactiver l'espacement des cellules
// et ignore la valeur de la propriété "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// L'ajustement de la propriété "CellSpacing" activera automatiquement l'espacement des cellules.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

Montre comment créer des paramètres de style personnalisés pour le tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// La définition des propriétés de style d'un tableau peut affecter les propriétés du tableau lui-même.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


