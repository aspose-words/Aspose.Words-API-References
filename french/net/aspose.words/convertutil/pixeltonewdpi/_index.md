---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words pour .NET
description: Transformez facilement les résolutions de pixels grâce à la méthode PixelToNewDpi de ConvertUtil. Obtenez une qualité d'image et une précision optimales pour vos projets.
type: docs
weight: 30
url: /fr/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Convertit les pixels d'une résolution à une autre.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pixels | Double | La valeur à convertir. |
| oldDpi | Double | La résolution dpi (points par pouce) actuelle. |
| newDpi | Double | La nouvelle résolution dpi (points par pouce). |

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
