---
title: Class HyphenationOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Settings.HyphenationOptions clase. Permite configurar las opciones de separación de palabras del documento.
type: docs
weight: 5790
url: /es/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Permite configurar las opciones de separación de palabras del documento.

Para obtener más información, visite el[Trabajar con separación de palabras](https://docs.aspose.com/words/net/working-with-hyphenation/) artículo de documentación.

```csharp
public class HyphenationOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Obtiene o establece el valor que determina si la separación de palabras automática está activada para el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Obtiene o establece el número máximo de líneas consecutivas que pueden terminar con guiones. El valor predeterminado para esta propiedad es 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Obtiene o establece el valor que determina si las palabras escritas en letras mayúsculas están divididas con guiones. El valor predeterminado para esta propiedad es`verdadero` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Obtiene o establece la distancia en 1/20 de un punto desde el margen derecho dentro del cual no desea que separe las palabras con guiones. El valor predeterminado para esta propiedad es 360 (0,25 pulgadas). |

### Ejemplos

Muestra cómo configurar la separación de palabras automática.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)


