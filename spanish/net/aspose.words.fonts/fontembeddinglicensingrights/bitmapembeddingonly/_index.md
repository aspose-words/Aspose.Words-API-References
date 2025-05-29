---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words para .NET
description: Descubra la propiedad FontEmbeddingLicensingRights BitmapEmbeddingOnly, que garantiza restricciones de incrustación de mapas de bits exclusivas para un mejor control del diseño.
type: docs
weight: 10
url: /es/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

Indica la restricción "Solo incrustación de mapa de bits".

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## Observaciones

Cuando este bit está activado, solo se pueden incrustar los mapas de bits contenidos en la fuente. No se pueden incrustar datos de contorno. Si no hay mapas de bits disponibles en la fuente, esta se considera no incrustable y los servicios de incrustación fallarán. También se aplican otras restricciones de incrustación.

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

* class [FontEmbeddingLicensingRights](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
