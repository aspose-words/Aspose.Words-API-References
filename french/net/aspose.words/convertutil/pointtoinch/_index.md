---
title: ConvertUtil.PointToInch
linktitle: PointToInch
articleTitle: PointToInch
second_title: Aspose.Words pour .NET
description: Convertissez facilement des points en pouces grâce à la méthode PointToInch de ConvertUtil. Simplifiez vos mesures et améliorez la précision de vos conceptions dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

Convertit les points en pouces.

```csharp
public static double PointToInch(double points)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| points | Double | La valeur à convertir. |

## Remarques

1 pouce équivaut à 72 points.

## Exemples

Montre comment spécifier les propriétés de la page en pouces.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La « Mise en page » d'une section définit la taille des marges de la page en points.
// Nous pouvons également utiliser la classe « ConvertUtil » pour utiliser une unité de mesure plus familière,
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

* class [ConvertUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
