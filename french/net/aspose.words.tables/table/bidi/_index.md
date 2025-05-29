---
title: Table.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words pour .NET
description: Découvrez les propriétés Table Bidi pour un formatage fluide des tableaux de droite à gauche. Améliorez votre site web grâce à des options de personnalisation faciles !
type: docs
weight: 80
url: /fr/net/aspose.words.tables/table/bidi/
---
## Table.Bidi property

Obtient ou définit s'il s'agit d'un tableau de droite à gauche.

```csharp
public bool Bidi { get; set; }
```

## Remarques

Quand`vrai`, les cellules de cette ligne sont disposées de droite à gauche.

La valeur par défaut est`FAUX`.

## Exemples

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

// La définition des propriétés de style d'une table peut affecter les propriétés de la table elle-même.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
