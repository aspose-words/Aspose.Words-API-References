---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: Aspose.Words para .NET
description: Optimice el diseño del texto con la propiedad HyphenationZone. Controle la separación de palabras desde el margen derecho para obtener documentos más limpios y profesionales.
type: docs
weight: 50
url: /es/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Obtiene o establece la distancia en 1/20 de un punto desde el margen derecho dentro del cual no desea separar palabras con guiones. El valor predeterminado para esta propiedad es 360 (0,25 pulgadas).

```csharp
public int HyphenationZone { get; set; }
```

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
