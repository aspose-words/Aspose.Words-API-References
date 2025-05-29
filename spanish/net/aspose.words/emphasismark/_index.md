---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.EmphasisMark, que incluye diversos tipos de énfasis para mejorar el formato de sus documentos. ¡Mejore el impacto de su texto hoy mismo!
type: docs
weight: 1870
url: /es/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Especifica los tipos posibles de marca de énfasis.

```csharp
public enum EmphasisMark
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Sin marca de énfasis. |
| OverSolidCircle | `1` | El signo de énfasis es un círculo negro sólido que se muestra encima del texto. |
| OverComma | `2` | El signo de énfasis es un carácter de coma que se muestra encima del texto. |
| OverWhiteCircle | `3` | El signo de énfasis es un círculo blanco vacío que se muestra encima del texto. |
| UnderSolidCircle | `4` | El signo de énfasis es un círculo negro sólido que se muestra debajo del texto. |

## Ejemplos

Muestra cómo agregar caracteres adicionales representados encima o debajo del carácter de glifo.

```csharp
DocumentBuilder builder = new DocumentBuilder();

//Posibles tipos de marca de énfasis:
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
