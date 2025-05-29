---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words para .NET
description: Descubre la propiedad Zip64Mode de OoxmlSaveOptions para mejorar la salida de tus documentos con el formato ZIP64. ¡Optimiza archivos grandes sin esfuerzo!
type: docs
weight: 80
url: /es/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

Especifica si se deben utilizar o no extensiones de formato ZIP64 para el documento de salida. El valor predeterminado esNever .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

## Ejemplos

Muestra cómo utilizar las extensiones de formato ZIP64.

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

### Ver también

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
