---
title: HyphenationOptions.ConsecutiveHyphenLimit
linktitle: ConsecutiveHyphenLimit
articleTitle: ConsecutiveHyphenLimit
second_title: Aspose.Words para .NET
description: Descubra la propiedad ConsecutiveHyphenLimit en HyphenationOptions. Controle el uso de guiones en su texto para mejorar la legibilidad y el formato. Valor predeterminado: 0.
type: docs
weight: 30
url: /es/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Obtiene o establece el número máximo de líneas consecutivas que pueden terminar con guiones. El valor predeterminado para esta propiedad es 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

## Observaciones

Si el valor de esta propiedad se establece en 0, cualquier número de líneas consecutivas puede terminar con guiones.

La propiedad no tiene efecto al guardar en formatos de página fijos, por ejemplo, PDF.

## Ejemplos

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

* class [HyphenationOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
