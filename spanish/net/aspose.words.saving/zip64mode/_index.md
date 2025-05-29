---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.Zip64Mode para un uso eficiente del formato ZIP64 en archivos OOXML, mejorando la gestión del tamaño de archivo y la compatibilidad.
type: docs
weight: 6550
url: /es/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

Especifica cuándo utilizar extensiones de formato ZIP64 para archivos OOXML.

```csharp
public enum Zip64Mode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Never | `0` | No utilice extensiones de formato ZIP64. |
| IfNecessary | `1` | Si es necesario utilice extensiones de formato ZIP64. |
| Always | `2` | Utilice siempre extensiones de formato ZIP64. |

## Observaciones

El archivo OOXML es un archivo ZIP que tiene un límite de 4 GB (2^32 bytes) en el tamaño sin comprimir de un archivo, el tamaño comprimido de un archivo y el tamaño total del archivo, así como un límite de 65.535 (2^16-1) archivos en el archivo. Las extensiones de formato ZIP64 aumentan los límites a 2^64.

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

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
