---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.Zip64Mode pour une utilisation efficace du format ZIP64 dans les fichiers OOXML, améliorant la gestion de la taille des fichiers et la compatibilité.
type: docs
weight: 6550
url: /fr/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

Spécifie quand utiliser les extensions de format ZIP64 pour les fichiers OOXML.

```csharp
public enum Zip64Mode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Never | `0` | N'utilisez pas les extensions au format ZIP64. |
| IfNecessary | `1` | Si nécessaire, utilisez les extensions au format ZIP64. |
| Always | `2` | Utilisez toujours les extensions au format ZIP64. |

## Remarques

Le fichier OOXML est une archive ZIP qui a une limite de 4 Go (2^32 octets) sur la taille non compressée d'un fichier, la taille compressée d'un fichier et la taille totale de l'archive, ainsi qu'une limite de 65 535 (2^16-1) fichiers dans l'archive. Les extensions de format ZIP64 augmentent les limites à 2^64.

## Exemples

Montre comment utiliser les extensions de format ZIP64.

```csharp
Random random = new Random();
DocumentBuilder builder = new DocumentBuilder();

for (int i = 0; i < 10000; i++)
{
    using (Bitmap bmp = new Bitmap(5, 5))
    using (Graphics g = Graphics.FromImage(bmp))
    {
        g.Clear(Color.FromArgb(random.Next(0, 254), random.Next(0, 254), random.Next(0, 254)));
        using (MemoryStream ms = new MemoryStream())
        {
            bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Png);
            builder.InsertImage(ms.ToArray());
        }
    }
}

builder.Document.Save(ArtifactsDir + "OoxmlSaveOptions.Zip64ModeOption.docx", 
    new OoxmlSaveOptions { Zip64Mode = Zip64Mode.Always });
```

### Voir également

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
