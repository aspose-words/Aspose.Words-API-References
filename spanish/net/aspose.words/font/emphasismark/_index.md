---
title: Font.EmphasisMark
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Obtiene o establece la marca de énfasis aplicada a este formato.
type: docs
weight: 110
url: /es/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Obtiene o establece la marca de énfasis aplicada a este formato.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

### Ejemplos

Muestra cómo agregar caracteres adicionales representados encima/debajo del carácter de glifo.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Posibles tipos de marca de énfasis:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Ver también

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


