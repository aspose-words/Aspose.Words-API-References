---
title: TableStyle.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TableStyle Bidi pour gérer facilement les styles de tableau de droite à gauche, améliorant ainsi votre mise en page pour une meilleure lisibilité et une meilleure expérience utilisateur.
type: docs
weight: 30
url: /fr/net/aspose.words/tablestyle/bidi/
---
## TableStyle.Bidi property

Obtient ou définit s'il s'agit d'un style pour un tableau de droite à gauche.

```csharp
public bool Bidi { get; set; }
```

## Remarques

Quand`vrai`, les cellules des rangées sont disposées de droite à gauche.

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

* class [TableStyle](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
