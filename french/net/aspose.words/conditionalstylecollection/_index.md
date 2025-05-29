---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.ConditionalStyleCollection pour gérer efficacement les objets ConditionalStyle, améliorant ainsi la mise en forme et la personnalisation des documents.
type: docs
weight: 520
url: /fr/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Représente une collection de[`ConditionalStyle`](../conditionalstyle/) objets.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article de documentation.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Obtient le style de cellule en bas à gauche. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Obtient le style de cellule en bas à droite. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Obtient le nombre de styles conditionnels dans la collection. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Obtient le style de bande de colonne paire. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Obtient le style de bande de ligne paire. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Obtient le style de la première colonne. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Obtient le style de la première ligne. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Récupère un[`ConditionalStyle`](../conditionalstyle/) objet par type de style conditionnel. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Obtient le style de la dernière colonne. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Obtient le style de la dernière ligne. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Obtient le style de bande de colonne impaire. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Obtient le style de bande de ligne impaire. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Obtient le style de cellule en haut à gauche. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Obtient le style de cellule en haut à droite. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Efface tous les styles conditionnels du style de tableau. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les styles conditionnels de la collection. |

## Remarques

Il n'est pas possible d'ajouter ou de supprimer des éléments de cette collection. Elle contient un ensemble permanent d'éléments : un élément pour chaque valeur de la[`ConditionalStyleType`](../conditionalstyletype/) type d'énumération.

## Exemples

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

// Créer un style de tableau personnalisé.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Les styles conditionnels sont des modifications de formatage qui affectent uniquement certaines cellules du tableau
// basé sur un prédicat, tel que les cellules se trouvant dans la dernière ligne.
// Vous trouverez ci-dessous trois manières d'accéder aux styles conditionnels d'un style de tableau à partir de la collection « ConditionalStyles ».
// 1 - Par type de style :
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Par index :
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - En tant que propriété :
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Appliquer le remplissage et la mise en forme du texte aux styles conditionnels.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Répertoriez toutes les conditions de style possibles.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Appliquez le style personnalisé, qui contient tous les styles conditionnels, au tableau.
table.Style = tableStyle;

// Notre style applique certains styles conditionnels par défaut.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Nous devrons activer tous les autres styles nous-mêmes via la propriété « StyleOptions ».
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Voir également

* class [ConditionalStyle](../conditionalstyle/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
