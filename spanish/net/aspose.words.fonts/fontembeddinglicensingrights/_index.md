---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.FontEmbeddingLicensingRights para administrar los derechos de incrustación de fuentes sin esfuerzo y mejorar la presentación de su documento.
type: docs
weight: 3310
url: /es/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

Representa los derechos de licencia de incrustación para la fuente.

```csharp
public class FontEmbeddingLicensingRights
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | Indica la restricción "Solo incrustación de mapa de bits". |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | Permisos de uso. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | Indica la restricción "Sin subconjuntos". |

## Observaciones

Para obtener más información, visite el [Sección de especificaciones OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) en el portal de tipografía de Microsoft.

## Ejemplos

Muestra cómo obtener información sobre los derechos de licencia para fuentes integradas (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// Obtener la lista de fuentes del documento.
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

### Ver también

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
