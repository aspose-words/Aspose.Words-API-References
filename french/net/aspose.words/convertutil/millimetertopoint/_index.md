---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
articleTitle: MillimeterToPoint
second_title: Aspose.Words pour .NET
description: Convertissez facilement des millimètres en points grâce à la méthode MillimeterToPoint de ConvertUtil. Simplifiez vos calculs de conception dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Convertit les millimètres en points.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| millimeters | Double | La valeur à convertir. |

## Remarques

1 pouce équivaut à 25,4 millimètres. 1 pouce équivaut à 72 points.

## Exemples

Montre comment spécifier les propriétés de la page en millimètres.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La « Mise en page » d'une section définit la taille des marges de la page en points.
// Nous pouvons également utiliser la classe « ConvertUtil » pour utiliser une unité de mesure plus familière,
// comme les millimètres lors de la définition des limites.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// Un centimètre vaut environ 28,3 points.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Ajoutez du contenu pour démontrer les nouvelles marges.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### Voir également

* class [ConvertUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
