---
title: Table.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser facilement l'apparence de votre table avec la propriété Style de table  améliorez vos conceptions avec des styles uniques sans effort !
type: docs
weight: 270
url: /fr/net/aspose.words.tables/table/style/
---
## Table.Style property

Obtient ou définit le style de tableau appliqué à ce tableau.

```csharp
public Style Style { get; set; }
```

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

* class [Style](../../../aspose.words/style/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
