---
title: ConditionalStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente une mise en forme spéciale appliquée à une zone dun tableau avec un style de tableau attribué.
type: docs
weight: 300
url: /fr/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Représente une mise en forme spéciale appliquée à une zone d'un tableau avec un style de tableau attribué.

```csharp
public sealed class ConditionalStyle
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders) { get; } | Obtient la collection de bordures de cellule par défaut pour le style conditionnel. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau. |
| [Font](../../aspose.words/conditionalstyle/font) { get; } | Obtient la mise en forme des caractères du style conditionnel. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat) { get; } | Obtient la mise en forme de paragraphe du style conditionnel. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau. |
| [Shading](../../aspose.words/conditionalstyle/shading) { get; } | Obtient un[`Shading`](../shading) objet qui fait référence à la mise en forme d'ombrage pour ce style conditionnel. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding) { get; set; } | Obtient ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau. |
| [Type](../../aspose.words/conditionalstyle/type) { get; } | Obtient la zone de tableau à laquelle ce style conditionnel se rapporte. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting)() | Efface la mise en forme de ce style conditionnel. |
| override [Equals](../../aspose.words/conditionalstyle/equals)(object) |  |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode)() | Calcule le code de hachage pour cet objet. |

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

* espace de noms [Aspose.Words](../../aspose.words)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
