---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: Aspose.Words pour .NET
description: Personnalisez vos tableaux sans effort avec la méthode SetBorders, en ajustant le style de ligne, la largeur et la couleur pour un look professionnel et soigné.
type: docs
weight: 440
url: /fr/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Définit toutes les bordures du tableau selon le style de ligne, la largeur et la couleur spécifiés.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| lineStyle | LineStyle | Le style de ligne à appliquer. |
| lineWidth | Double | La largeur de ligne à définir (en points). |
| color | Color | La couleur à utiliser pour la bordure. |

## Exemples

Montre comment formater toutes les bordures d'un tableau à la fois.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Effacer toutes les bordures existantes du tableau.
table.ClearBorders();

// Définissez une seule ligne verte pour servir de bordure extérieure et intérieure de ce tableau.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Montre comment appliquer la couleur de bordure et d'ombrage lors de la création d'un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Démarrez un tableau et définissez une couleur/épaisseur par défaut pour ses bordures.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Créez une ligne avec deux cellules avec des couleurs d'arrière-plan différentes.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Réinitialiser la mise en forme des cellules pour désactiver les couleurs d'arrière-plan
// définir une épaisseur de bordure personnalisée pour toutes les nouvelles cellules créées par le générateur,
// puis construisez une deuxième ligne.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Voir également

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
