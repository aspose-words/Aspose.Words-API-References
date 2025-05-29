---
title: PhysicalFontInfo.FullFontName
linktitle: FullFontName
articleTitle: FullFontName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FullFontName de PhysicalFontInfo pour accéder facilement aux noms de polices. Améliorez votre typographie grâce à une identification précise des polices !
type: docs
weight: 40
url: /fr/net/aspose.words.fonts/physicalfontinfo/fullfontname/
---
## PhysicalFontInfo.FullFontName property

Nom complet de la police.

```csharp
public string FullFontName { get; }
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
