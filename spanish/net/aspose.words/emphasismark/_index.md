---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words para .NET
description: Aspose.Words.EmphasisMark enumeración. Especifica posibles tipos de marca de énfasis en C#.
type: docs
weight: 1460
url: /es/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Especifica posibles tipos de marca de énfasis.

```csharp
public enum EmphasisMark
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Sin marca de énfasis. |
| OverSolidCircle | `1` | La marca de énfasis es un círculo negro sólido que se muestra encima del texto. |
| OverComma | `2` | La marca de énfasis es un carácter de coma que se muestra encima del texto. |
| OverWhiteCircle | `3` | La marca de énfasis es un círculo blanco vacío que se muestra encima del texto. |
| UnderSolidCircle | `4` | La marca de énfasis es un círculo negro sólido que se muestra debajo del texto. |

## Ejemplos

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
