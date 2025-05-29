---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words pour .NET
description: Découvrez les droits de licence d'incorporation de polices sans sous-ensemble. Assurez la conformité et protégez vos polices tout en améliorant vos projets de conception.
type: docs
weight: 30
url: /fr/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

Indique la restriction « Aucun sous-ensemble ».

```csharp
public bool NoSubsetting { get; }
```

## Remarques

Lorsque cette option est activée, la police ne doit pas être modifiée avant l'intégration. D'autres restrictions d'intégration s'appliquent également.

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
