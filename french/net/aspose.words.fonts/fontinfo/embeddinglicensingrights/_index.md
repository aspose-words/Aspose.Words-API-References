---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FontInfo EmbeddingLicensingRights pour accéder et gérer facilement vos droits de licence de polices intégrées pour une intégration de conception transparente.
type: docs
weight: 30
url: /fr/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

Obtient les droits de licence des polices intégrées.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Remarques

La valeur peut être nulle si la police n'est pas intégrée.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
