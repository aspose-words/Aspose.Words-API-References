---
title: HyphenationOptions.HyphenateCaps
second_title: Referencia de API de Aspose.Words para .NET
description: HyphenationOptions propiedad. Obtiene o establece el valor que determina si las palabras escritas en mayúsculas están separadas por guiones. El valor predeterminado para esta propiedad es verdadero .
type: docs
weight: 40
url: /es/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Obtiene o establece el valor que determina si las palabras escritas en mayúsculas están separadas por guiones. El valor predeterminado para esta propiedad es **verdadero** .

```csharp
public bool HyphenateCaps { get; set; }
```

### Ejemplos

Muestra cómo configurar la partición automática.

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
* espacio de nombres [Aspose.Words.Settings](../../hyphenationoptions/)
* asamblea [Aspose.Words](../../../)


