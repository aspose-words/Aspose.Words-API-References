---
title: FontEmbeddingLicensingRights.EmbeddingUsagePermissions
linktitle: EmbeddingUsagePermissions
articleTitle: EmbeddingUsagePermissions
second_title: Aspose.Words pour .NET
description: Libérez votre potentiel créatif grâce aux droits de licence d'intégration de polices. Explorez les autorisations d'utilisation pour une intégration fluide des polices dans vos projets.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/
---
## FontEmbeddingLicensingRights.EmbeddingUsagePermissions property

Autorisations d'utilisation.

```csharp
public FontEmbeddingUsagePermissions EmbeddingUsagePermissions { get; }
```

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

* enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* class [FontEmbeddingLicensingRights](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
