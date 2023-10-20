---
title: Document.HyphenationOptions
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words para .NET
description: Document HyphenationOptions propiedad. Proporciona acceso a las opciones de separación de palabras del documento en C#.
type: docs
weight: 210
url: /es/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

Proporciona acceso a las opciones de separación de palabras del documento.

```csharp
public HyphenationOptions HyphenationOptions { get; }
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

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
