---
title: BorderCollection.Bottom
second_title: Référence de l'API Aspose.Words pour .NET
description: BorderCollection propriété. Obtient la bordure inférieure.
type: docs
weight: 10
url: /fr/net/aspose.words/bordercollection/bottom/
---
## BorderCollection.Bottom property

Obtient la bordure inférieure.

```csharp
public Border Bottom { get; }
```

### Exemples

Montre comment appliquer une couleur de bordure et d'ombrage lors de la création d'un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Démarre un tableau et définit une couleur/épaisseur par défaut pour ses bordures.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Crée une ligne avec deux cellules avec des couleurs d'arrière-plan différentes.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Réinitialiser le formatage des cellules pour désactiver les couleurs d'arrière-plan
// définit une épaisseur de bordure personnalisée pour toutes les nouvelles cellules créées par le constructeur,
// puis construire une deuxième ligne.
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
* espace de noms [Aspose.Words](../../bordercollection/)
* Assemblée [Aspose.Words](../../../)


