---
title: ConvertUtil Class
linktitle: ConvertUtil
articleTitle: ConvertUtil
second_title: Aspose.Words pour .NET
description: Aspose.Words.ConvertUtil classe. Fournit des fonctions dassistance pour convertir entre différentes unités de mesure en C#.
type: docs
weight: 360
url: /fr/net/aspose.words/convertutil/
---
## ConvertUtil class

Fournit des fonctions d'assistance pour convertir entre différentes unités de mesure.

Pour en savoir plus, visitez le[Convertir entre les unités de mesure](https://docs.aspose.com/words/net/convert-between-measurement-units/) article documentaire.

```csharp
public static class ConvertUtil
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [InchToPoint](../../aspose.words/convertutil/inchtopoint/)(*double*) | Convertit les pouces en points. |
| static [MillimeterToPoint](../../aspose.words/convertutil/millimetertopoint/)(*double*) | Convertit les millimètres en points. |
| static [PixelToNewDpi](../../aspose.words/convertutil/pixeltonewdpi/)(*double, double, double*) | Convertit les pixels d'une résolution à une autre. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint)(*double*) | Convertit les pixels en points à 96 dpi. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint_1)(*double, double*) | Convertit les pixels en points à la résolution de pixels spécifiée. |
| static [PointToInch](../../aspose.words/convertutil/pointtoinch/)(*double*) | Convertit les points en pouces. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel)(*double*) | Convertit les points en pixels à 96 dpi. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel_1)(*double, double*) | Convertit les points en pixels à la résolution de pixels spécifiée. |

## Exemples

Montre comment ajuster le format du papier, l’orientation, les marges, ainsi que d’autres paramètres pour une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Montre comment spécifier les propriétés de la page en pouces.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La "Mise en page" d'une section définit la taille des marges de la page en points.
// On peut également utiliser la classe "ConvertUtil" pour utiliser une unité de mesure plus familière,
// comme les pouces lors de la définition des limites.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Un pouce vaut 72 points.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Ajoutez du contenu pour démontrer les nouvelles marges.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
