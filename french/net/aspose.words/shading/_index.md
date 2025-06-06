---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Shading, conçue pour améliorer vos documents avec des attributs d'ombrage personnalisables pour un aspect professionnel.
type: docs
weight: 6820
url: /fr/net/aspose.words/shading/
---
## Shading class

Contient les attributs d'ombrage d'un objet.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class Shading : InternableComplexAttr
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Obtient ou définit la couleur appliquée à l'arrière-plan du`Shading` objet. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Obtient ou définit la couleur du thème du motif d'arrière-plan dans le jeu de couleurs appliqué qui est associé à ceci`Shading` objet. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur de thème d'arrière-plan. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Obtient ou définit la couleur appliquée au premier plan de l'`Shading` objet. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Obtient ou définit la couleur du thème du motif de premier plan dans le jeu de couleurs appliqué qui est associé à cela`Shading` objet. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Obtient ou définit la texture d'ombrage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Supprime l'ombrage de l'objet. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Détermine si le spécifié`Shading` est égal en valeur au courant`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Sert de fonction de hachage pour ce type. |

## Exemples

Montre comment décorer du texte avec des bordures et des ombrages.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
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

* class [InternableComplexAttr](../internablecomplexattr/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
