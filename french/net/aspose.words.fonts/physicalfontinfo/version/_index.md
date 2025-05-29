---
title: PhysicalFontInfo.Version
linktitle: Version
articleTitle: Version
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Version PhysicalFontInfo, accédez facilement à la chaîne de version de la police pour une cohérence de conception améliorée et une typographie améliorée.
type: docs
weight: 50
url: /fr/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

Chaîne de version de la police.

```csharp
public string Version { get; }
```

## Exemples

Montre comment répertorier les polices disponibles.

```csharp
// Configurez Aspose.Words pour rechercher des polices à partir d'un dossier personnalisé, puis imprimez toutes les polices disponibles.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Voir également

* class [PhysicalFontInfo](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
