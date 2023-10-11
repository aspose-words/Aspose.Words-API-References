---
title: Font.Italic
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Verdadero si la fuente tiene el formato de cursiva.
type: docs
weight: 160
url: /es/net/aspose.words/font/italic/
---
## Font.Italic property

Verdadero si la fuente tiene el formato de cursiva.

```csharp
public bool Italic { get; set; }
```

### Ejemplos

Muestra cómo escribir texto en cursiva utilizando un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


