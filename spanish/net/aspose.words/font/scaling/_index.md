---
title: Font.Scaling
linktitle: Scaling
articleTitle: Scaling
second_title: Aspose.Words para .NET
description: Font Scaling propiedad. Obtiene o establece la escala del ancho de caracteres en porcentaje en C#.
type: docs
weight: 310
url: /es/net/aspose.words/font/scaling/
---
## Font.Scaling property

Obtiene o establece la escala del ancho de caracteres en porcentaje.

```csharp
public int Scaling { get; set; }
```

## Ejemplos

Muestra cómo configurar la escala horizontal y el espaciado de los caracteres.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue una corrida de texto y aumente el ancho de los caracteres al 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Agregue una corrida de texto y agregue 1 punto de espacio horizontal adicional entre cada carácter.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Añade una corrida de texto y acerca los caracteres en 1 punto.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
