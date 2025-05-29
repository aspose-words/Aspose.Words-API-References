---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words pour .NET
description: Convertissez facilement SaveFormat en LoadFormat grâce à la méthode FileFormatUtil. Simplifiez la gestion de vos fichiers et améliorez la compatibilité dès aujourd'hui !
type: docs
weight: 90
url: /fr/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Convertit un[`SaveFormat`](../../saveformat/) valeur à un[`LoadFormat`](../../loadformat/) valeur si possible.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | Lancer quand on ne peut pas convertir. |

## Exemples

Montre comment convertir un format de sauvegarde en son format de chargement correspondant.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Certains types de fichiers peuvent contenir des documents enregistrés, mais pas chargés à partir d'Aspose.Words.
// Si nous tentons de convertir un format de sauvegarde d'un tel type en un format de chargement, une exception sera levée.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Voir également

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
