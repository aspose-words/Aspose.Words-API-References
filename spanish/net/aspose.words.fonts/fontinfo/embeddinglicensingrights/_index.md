---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words para .NET
description: Descubra la propiedad FontInfo EmbeddingLicensingRights para acceder y administrar fácilmente sus derechos de licencia de fuentes integradas para una integración de diseño perfecta.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

Obtiene los derechos de licencia de fuentes incrustadas.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## Observaciones

El valor puede ser nulo si la fuente no está incrustada.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
