---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Fonts.FontEmbeddingUsagePermissions, que permite un control preciso sobre los permisos de incrustación de fuentes para una mejor gestión de documentos.
type: docs
weight: 3320
url: /es/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

Representa los permisos de uso de incrustación de fuentes.

```csharp
public enum FontEmbeddingUsagePermissions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Installable | `0` | La fuente puede estar incrustada y puede instalarse permanentemente para su uso en sistemas remotos o para su uso por otros usuarios. |
| RestrictedLicense | `1` | La fuente no debe modificarse, incrustarse ni intercambiarse de ninguna manera sin obtener primero el permiso explícito del propietario legal. |
| PrintAndPreview | `2` | La fuente puede estar incrustada y cargada temporalmente en otros sistemas con el fin de visualizar o imprimir el documento. |
| Editable | `3` | La fuente puede estar incrustada y cargada temporalmente en otros sistemas. |

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
