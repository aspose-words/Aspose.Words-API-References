---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.FontEmbeddingLicensingRights pour gérer les droits d'intégration des polices sans effort et améliorer la présentation de votre document.
type: docs
weight: 3310
url: /fr/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

Représente les droits de licence d'intégration pour la police.

```csharp
public class FontEmbeddingLicensingRights
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | Indique la restriction « Incorporation de bitmap uniquement ». |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | Autorisations d'utilisation. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | Indique la restriction « Aucun sous-ensemble ». |

## Remarques

Pour en savoir plus, visitez le [Section de spécification OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) sur le portail Microsoft Typography.

## Exemples

Montre comment obtenir des informations sur les droits de licence pour les polices intégrées (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Obtenir la liste des polices du document.
FontInfoCollection fontInfos = doc.FontInfos;
foreach (FontInfo fontInfo in fontInfos) 
{
    if (fontInfo.EmbeddingLicensingRights != null)
    {
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.EmbeddingUsagePermissions);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.BitmapEmbeddingOnly);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.NoSubsetting);
    }
}
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
