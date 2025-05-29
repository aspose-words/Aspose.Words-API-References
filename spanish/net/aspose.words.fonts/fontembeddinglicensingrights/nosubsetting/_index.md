---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words para .NET
description: Descubra los derechos de licencia para incrustar fuentes sin subconjuntos. Garantice el cumplimiento normativo y proteja sus fuentes mientras optimiza sus proyectos de diseño.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

Indica la restricción "Sin subconjuntos".

```csharp
public bool NoSubsetting { get; }
```

## Observaciones

Cuando esta opción está activada, no se debe crear un subconjunto de la fuente antes de la incrustación. También se aplican otras restricciones de incrustación.

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
