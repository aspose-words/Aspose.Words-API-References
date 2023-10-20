---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words para .NET
description: Font NoProofing propiedad. Verdadero cuando los caracteres formateados no deben revisarse la ortografía en C#.
type: docs
weight: 280
url: /es/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Verdadero cuando los caracteres formateados no deben revisarse la ortografía.

```csharp
public bool NoProofing { get; set; }
```

## Ejemplos

Muestra cómo evitar que Microsoft Word revise la ortografía del texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalmente, Microsoft Word enfatiza los errores ortográficos con un subrayado rojo irregular.
// Podemos desactivar el indicador "NoProofing" para crear una porción de texto que
// omite el corrector ortográfico y lo desactiva por completo.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
