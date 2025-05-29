---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.PhysicalFontInfo, qui fournit des détails essentiels sur les polices physiques pour un traitement et une conception de documents améliorés.
type: docs
weight: 3460
url: /fr/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Spécifie les informations sur la police physique disponible pour le moteur de polices Aspose.Words.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public class PhysicalFontInfo
```

## Propriétés

| Nom | La description |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | Incorporation des droits de licence pour la police. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Chemin vers le fichier de police, le cas échéant. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Nom de famille de la police. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Nom complet de la police. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Chaîne de version de la police. |

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

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
