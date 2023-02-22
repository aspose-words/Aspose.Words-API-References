---
title: Enum EmphasisMark
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.EmphasisMark enumeración. Especifica los posibles tipos de marcas de énfasis.
type: docs
weight: 1310
url: /es/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Especifica los posibles tipos de marcas de énfasis.

```csharp
public enum EmphasisMark
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Sin marca de énfasis. |
| OverSolidCircle | `1` | La marca de énfasis es un círculo negro sólido que se muestra sobre el texto. |
| OverComma | `2` | La marca de énfasis es un carácter de coma que se muestra encima del texto. |
| OverWhiteCircle | `3` | La marca de énfasis es un círculo blanco vacío que se muestra sobre el texto. |
| UnderSolidCircle | `4` | La marca de énfasis es un círculo negro sólido que se muestra debajo del texto. |

### Ejemplos

Muestra cómo agregar caracteres adicionales representados arriba/abajo del carácter de glifo.

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


