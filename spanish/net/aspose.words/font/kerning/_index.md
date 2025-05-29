---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words para .NET
description: Descubre la propiedad de kerning de fuentes y controla cuándo comienza el kerning para optimizar la claridad y el diseño del texto. ¡Mejora tu tipografía con precisión!
type: docs
weight: 180
url: /es/net/aspose.words/font/kerning/
---
## Font.Kerning property

Obtiene o establece el tamaño de fuente en el que se inicia el kerning.

```csharp
public double Kerning { get; set; }
```

## Ejemplos

Muestra cómo especificar el tamaño de fuente en el que el kerning comienza a tener efecto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Establezca el tamaño de fuente del constructor y el tamaño mínimo en el que se aplicará el kerning.
// El tamaño de la fuente cae por debajo del umbral de kerning, por lo que la siguiente línea no tendrá kerning.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Establezca el umbral de kerning para que el tamaño de fuente actual del constructor sea superior a éste.
// A cualquier texto que agreguemos a partir de este punto se le aplicará el kerning. Los espacios entre caracteres
// se ajustará, lo que normalmente dará como resultado un texto ligeramente más agradable a la vista.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
