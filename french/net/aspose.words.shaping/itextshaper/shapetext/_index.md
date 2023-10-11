---
title: ITextShaper.ShapeText
second_title: Référence de l'API Aspose.Words pour .NET
description: ITextShaper méthode. RetoursClusterobjets générés à partir dune séquence de fragments de texte. La longueur du tableau renvoyé est égale à la longueur deruns . Si lexécution sur un index a des clusters correspondants le résultat au même index les fera enregistrer.
type: docs
weight: 10
url: /fr/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Retours[`Cluster`](../../cluster/)objets générés à partir d'une séquence de fragments de texte. La longueur du tableau renvoyé est égale à la longueur de*runs* . Si l'exécution sur un index a des clusters correspondants, le résultat au même index les fera enregistrer.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| runs | String[] | Une séquence de fragments de texte |
| direction | Direction | Une direction de texte |
| script | UnicodeScript | Un scénario |
| fontFeatures | FontFeature[] | Un ensemble de fonctionnalités à considérer |

### Voir également

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* espace de noms [Aspose.Words.Shaping](../../itextshaper/)
* Assemblée [Aspose.Words](../../../)


