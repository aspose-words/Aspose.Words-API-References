---
title: TableStyle.RowStripe
linktitle: RowStripe
articleTitle: RowStripe
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TableStyle RowStripe pour personnaliser facilement les bandes de lignes paires/impaires pour une meilleure lisibilité du tableau et un attrait visuel amélioré.
type: docs
weight: 120
url: /fr/net/aspose.words/tablestyle/rowstripe/
---
## TableStyle.RowStripe property

Obtient ou définit un nombre de lignes à inclure dans la bande lorsque le style spécifie une bande de lignes impaires/paires.

```csharp
public int RowStripe { get; set; }
```

## Exemples

Montre comment créer des styles de tableau conditionnels qui alternent entre les lignes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons configurer un style conditionnel d'un tableau pour appliquer une couleur différente à la ligne/colonne,
// selon que la ligne/colonne est paire ou impaire, créant un motif de couleurs alternées.
// Nous pouvons également appliquer un nombre n au découpage des lignes/colonnes,
// ce qui signifie que la couleur alterne toutes les n lignes/colonnes au lieu d'une.
// Créez un tableau où les colonnes et les lignes simples seront groupées par trois.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Appliquer un style de ligne à toutes les bordures du tableau.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Définissez les deux couleurs, qui alterneront toutes les 3 lignes.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Définissez une couleur à appliquer à chaque colonne paire, qui remplacera toute coloration de ligne personnalisée.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// La propriété « StyleOptions » active les bandes de lignes par défaut.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Utilisez également la propriété « StyleOptions » pour activer les bandes de colonnes.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Voir également

* class [TableStyle](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
