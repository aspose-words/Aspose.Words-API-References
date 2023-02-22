---
title: ConditionalStyleCollection.Item
second_title: Référence de l'API Aspose.Words pour .NET
description: ConditionalStyleCollection propriété. Récupère unConditionalStyle objet par type de style conditionnel.
type: docs
weight: 80
url: /fr/net/aspose.words/conditionalstylecollection/item/
---
## ConditionalStyleCollection indexer (1 of 2)

Récupère un[`ConditionalStyle`](../../conditionalstyle/) objet par type de style conditionnel.

```csharp
public ConditionalStyle this[ConditionalStyleType conditionalStyleType] { get; }
```

### Exemples

Montre comment travailler avec certains styles de zone d'un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Crée un style de tableau personnalisé.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Les styles conditionnels sont des changements de mise en forme qui n'affectent que certaines cellules du tableau
// basé sur un prédicat, tel que les cellules se trouvant dans la dernière ligne.
// Vous trouverez ci-dessous trois façons d'accéder aux styles conditionnels d'un style de tableau à partir de la collection "ConditionalStyles".
// 1 - Par type de style :
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Par index :
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - En tant que propriété :
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Appliquez le rembourrage et la mise en forme du texte aux styles conditionnels.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Liste toutes les conditions de style possibles.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Applique le style personnalisé, qui contient tous les styles conditionnels, au tableau.
table.Style = tableStyle;

// Notre style applique certains styles conditionnels par défaut.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Nous devrons activer nous-mêmes tous les autres styles via la propriété "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Voir également

* class [ConditionalStyle](../../conditionalstyle/)
* enum [ConditionalStyleType](../../conditionalstyletype/)
* class [ConditionalStyleCollection](../)
* espace de noms [Aspose.Words](../../conditionalstylecollection/)
* Assemblée [Aspose.Words](../../../)

---

## ConditionalStyleCollection indexer (2 of 2)

Récupère un[`ConditionalStyle`](../../conditionalstyle/) objet par index.

```csharp
public ConditionalStyle this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Index de base zéro du style conditionnel à récupérer. |

### Exemples

Montre comment travailler avec certains styles de zone d'un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Crée un style de tableau personnalisé.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Les styles conditionnels sont des changements de mise en forme qui n'affectent que certaines cellules du tableau
// basé sur un prédicat, tel que les cellules se trouvant dans la dernière ligne.
// Vous trouverez ci-dessous trois façons d'accéder aux styles conditionnels d'un style de tableau à partir de la collection "ConditionalStyles".
// 1 - Par type de style :
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Par index :
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - En tant que propriété :
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Appliquez le rembourrage et la mise en forme du texte aux styles conditionnels.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Liste toutes les conditions de style possibles.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Applique le style personnalisé, qui contient tous les styles conditionnels, au tableau.
table.Style = tableStyle;

// Notre style applique certains styles conditionnels par défaut.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Nous devrons activer nous-mêmes tous les autres styles via la propriété "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Voir également

* class [ConditionalStyle](../../conditionalstyle/)
* class [ConditionalStyleCollection](../)
* espace de noms [Aspose.Words](../../conditionalstylecollection/)
* Assemblée [Aspose.Words](../../../)


