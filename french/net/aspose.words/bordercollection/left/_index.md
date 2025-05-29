---
title: BorderCollection.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BorderCollection Left, accédez et personnalisez sans effort la bordure gauche pour une flexibilité de conception et un attrait visuel améliorés.
type: docs
weight: 70
url: /fr/net/aspose.words/bordercollection/left/
---
## BorderCollection.Left property

Obtient la bordure gauche.

```csharp
public Border Left { get; }
```

## Exemples

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

* class [Border](../../border/)
* class [BorderCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
