---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font TextEffect para personalizar fácilmente las animaciones de fuentes y mejorar sus diseños con efectos de texto dinámicos para una experiencia de usuario cautivadora.
type: docs
weight: 460
url: /es/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Obtiene o establece el efecto de animación de fuente.

```csharp
public TextEffect TextEffect { get; set; }
```

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

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
