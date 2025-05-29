---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OoxmlSaveOptions Zip64Mode pour améliorer la sortie de vos documents au format ZIP64. Optimisez vos fichiers volumineux sans effort !
type: docs
weight: 80
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Spécifie s'il faut ou non utiliser les extensions de format ZIP64 pour le document de sortie. La valeur par défaut estNever .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

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

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
