---
title: ConvertUtil.PixelToPoint
linktitle: PixelToPoint
articleTitle: PixelToPoint
second_title: Aspose.Words pour .NET
description: Convertissez facilement des pixels en points à 96 ppp grâce à la méthode PixelToPoint de ConvertUtil. Améliorez la précision de vos créations dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words/convertutil/pixeltopoint/
---
## PixelToPoint(*double*) {#pixeltopoint}

Convertit les pixels en points à 96 dpi.

```csharp
public static double PixelToPoint(double pixels)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pixels | Double | La valeur à convertir. |

## Remarques

1 pouce équivaut à 72 points.

## Exemples

Montre comment spécifier les propriétés de la page en pixels.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La « Mise en page » d'une section définit la taille des marges de la page en points.
// Nous pouvons également utiliser la classe « ConvertUtil » pour utiliser une unité de mesure différente,
// comme les pixels lors de la définition des limites.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// Un pixel vaut 0,75 point.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// La valeur DPI par défaut utilisée est 96.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// Ajoutez du contenu pour démontrer les nouvelles marges.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Voir également

* class [ConvertUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## PixelToPoint(*double, double*) {#pixeltopoint_1}

Convertit les pixels en points à la résolution de pixels spécifiée.

```csharp
public static double PixelToPoint(double pixels, double resolution)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pixels | Double | La valeur à convertir. |
| resolution | Double | La résolution dpi (points par pouce). |

## Remarques

1 pouce équivaut à 72 points.

## Exemples

Montre comment utiliser la conversion de points en pixels avec une résolution par défaut et personnalisée.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez la taille de la marge supérieure de cette section en pixels, selon un DPI personnalisé.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Au DPI par défaut de 96, un pixel vaut 0,75 point.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Définissez un nouveau DPI et ajustez la valeur de la marge supérieure en conséquence.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Voir également

* class [ConvertUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
