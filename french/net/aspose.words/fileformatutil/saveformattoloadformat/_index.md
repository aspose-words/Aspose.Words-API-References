---
title: FileFormatUtil.SaveFormatToLoadFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: FileFormatUtil méthode. Convertit unSaveFormat valeur à unLoadFormat valeur si possible.
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
| ArgumentException | Lance quand on ne peut pas convertir. |

### Exemples

Montre comment convertir un format de sauvegarde en son format de chargement correspondant.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Certains types de fichiers peuvent contenir des documents enregistrés, mais non chargés à l'aide d'Aspose.Words.
// Si nous tentons de convertir un format de sauvegarde d'un tel type en un format de chargement, une exception sera levée.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Voir également

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../fileformatutil/)
* Assemblée [Aspose.Words](../../../)


