---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FontEmbeddingLicensingRights BitmapEmbeddingOnly, qui garantit des restrictions d'incorporation de bitmap exclusives pour un contrôle de conception amélioré.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

Indique la restriction « Incorporation de bitmap uniquement ».

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Remarques

Lorsque ce bit est activé, seules les bitmaps contenues dans la police peuvent être incorporées. Aucune donnée de contour ne peut être incorporée. Si aucune bitmap n'est disponible dans la police, celle-ci est considérée comme non incorporable et les services d'incorporation échoueront. D'autres restrictions d'incorporation s'appliquent également.

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

* class [FontEmbeddingLicensingRights](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
