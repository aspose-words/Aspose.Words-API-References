---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Fonts.FontEmbeddingUsagePermissions, permettant un contrôle précis des autorisations d'intégration des polices pour une gestion améliorée des documents.
type: docs
weight: 3320
url: /fr/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Représente les autorisations d'utilisation de l'intégration des polices.

```csharp
public enum FontEmbeddingUsagePermissions
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Installable | `0` | La police peut être intégrée et peut être installée de manière permanente pour être utilisée sur des systèmes distants ou pour être utilisée par d'autres utilisateurs. |
| RestrictedLicense | `1` | La police ne doit pas être modifiée, incorporée ou échangée de quelque manière que ce soit sans avoir obtenu au préalable l'autorisation explicite du propriétaire légal. |
| PrintAndPreview | `2` | La police peut être intégrée et peut être temporairement chargée sur d'autres systèmes à des fins de visualisation ou d'impression du document. |
| Editable | `3` | La police peut être intégrée et peut être chargée temporairement sur d'autres systèmes. |

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
