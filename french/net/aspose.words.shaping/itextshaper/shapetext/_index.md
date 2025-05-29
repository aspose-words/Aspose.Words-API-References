---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ShapeText d'iTextShaper, qui génère efficacement des objets Cluster à partir de fragments de texte, garantissant un formatage et un alignement précis du texte.
type: docs
weight: 10
url: /fr/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Retours[`Cluster`](../../cluster/)objets générés à partir d'une séquence de fragments de texte. La longueur du tableau renvoyé est égale à la longueur de*runs* . Si l'exécution à un index a des clusters correspondants, le résultat au même index les aura enregistrés.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| runs | String[] | Une séquence de fragments de texte |
| direction | Direction | Une direction de texte |
| script | UnicodeScript | Un script |
| enabledFontFeatures | FontFeature[] | Un ensemble de fonctionnalités OpenType explicitement activées à prendre en compte |
| variations | VariationAxisCoordinate[] | Valeurs de l'axe de variation de la police |

### Voir également

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* espace de noms [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* Assemblée [Aspose.Words](../../../)
