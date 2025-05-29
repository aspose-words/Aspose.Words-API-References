---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.ConditionalStyleType pour définir la mise en forme dynamique des tableaux. Améliorez le style de vos documents grâce à des options conditionnelles flexibles !
type: docs
weight: 530
url: /fr/net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

Représente les zones de tableau possibles pour lesquelles une mise en forme conditionnelle peut être définie dans un style de tableau.

```csharp
public enum ConditionalStyleType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| FirstRow | `0` | Spécifie la mise en forme de la première ligne d'un tableau. |
| FirstColumn | `1` | Spécifie la mise en forme de la première colonne d'un tableau. |
| LastRow | `2` | Spécifie la mise en forme de la dernière ligne d'un tableau. |
| LastColumn | `3` | Spécifie la mise en forme de la dernière colonne d'un tableau. |
| OddRowBanding | `4` | Spécifie le formatage de la bande de ligne impaire. |
| OddColumnBanding | `5` | Spécifie le formatage de la bande de colonnes impaires. |
| EvenRowBanding | `6` | Spécifie le formatage de la bande de lignes paires. |
| EvenColumnBanding | `7` | Spécifie la mise en forme de la bande de colonnes paires. |
| TopLeftCell | `8` | Spécifie la mise en forme de la cellule supérieure gauche d'un tableau. |
| TopRightCell | `9` | Spécifie la mise en forme de la cellule supérieure droite d'un tableau. |
| BottomLeftCell | `10` | Spécifie la mise en forme de la cellule en bas à gauche d'un tableau. |
| BottomRightCell | `11` | Spécifie la mise en forme de la cellule en bas à droite d'un tableau. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
