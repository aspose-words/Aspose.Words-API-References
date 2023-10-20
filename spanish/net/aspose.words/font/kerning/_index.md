---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words para .NET
description: Font Kerning propiedad. Obtiene o establece el tamaño de fuente en el que comienza el kerning en C#.
type: docs
weight: 180
url: /es/net/aspose.words/font/kerning/
---
## Font.Kerning property

Obtiene o establece el tamaño de fuente en el que comienza el kerning.

```csharp
public double Kerning { get; set; }
```

## Ejemplos

Muestra cómo especificar el tamaño de fuente a partir del cual el interletraje comienza a surtir efecto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Establece el tamaño de fuente del constructor y el tamaño mínimo en el que el kerning tendrá efecto.
// El tamaño de fuente cae por debajo del umbral de kerning, por lo que la siguiente ejecución no tendrá kerning.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Establece el umbral de kerning para que el tamaño de fuente actual del constructor esté por encima de él.
// A cualquier texto que agreguemos desde este punto se le aplicará el kerning. Los espacios entre personajes.
// se ajustará, lo que normalmente dará como resultado una ejecución de texto ligeramente más agradable desde el punto de vista estético.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
