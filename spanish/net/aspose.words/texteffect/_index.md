---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words para .NET
description: Explora la enumeración Aspose.Words.TextEffect para crear animaciones de texto dinámicas. Mejora tus documentos con efectos atractivos para una experiencia de usuario cautivadora.
type: docs
weight: 7270
url: /es/net/aspose.words/texteffect/
---
## TextEffect enumeration

Efecto de animación para ejecuciones de texto.

```csharp
public enum TextEffect
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## Ejemplos

Muestra cómo aplicar un efecto visual a una carrera.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Las versiones anteriores de Microsoft Word solo admiten efectos de animación de fuentes.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
