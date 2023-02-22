---
title: TableStyle.TopPadding
second_title: Référence de l'API Aspose.Words pour .NET
description: TableStyle propriété. Obtient ou définit la quantité despace en points à ajouter audessus du contenu des cellules du tableau.
type: docs
weight: 140
url: /fr/net/aspose.words/tablestyle/toppadding/
---
## TableStyle.TopPadding property

Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau.

```csharp
public double TopPadding { get; set; }
```

### Exemples

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

* class [TableStyle](../)
* espace de noms [Aspose.Words](../../tablestyle/)
* Assemblée [Aspose.Words](../../../)


