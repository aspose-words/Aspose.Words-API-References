---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.TextDmlEffect para mejorar las ejecuciones de texto con efectos DML dinámicos. ¡Mejore la presentación de sus documentos sin esfuerzo!
type: docs
weight: 7260
url: /es/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Efecto de texto Dml para ejecuciones de texto.

```csharp
public enum TextDmlEffect
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Glow | `0` | Efecto de resplandor, en el que se agrega un contorno borroso de color fuera de los bordes del objeto. |
| Fill | `1` | Efecto de superposición de relleno. |
| Shadow | `2` | Efecto de sombra. |
| Outline | `3` | Efecto de contorno. |
| Effect3D | `4` | Efecto 3D. |
| Reflection | `5` | Efecto de reflexión. |

## Ejemplos

Muestra cómo comprobar si una ejecución muestra un efecto de texto DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
