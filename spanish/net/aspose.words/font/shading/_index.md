---
title: Font.Shading
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Devuelve unShading objeto que hace referencia al formato de sombreado de la fuente.
type: docs
weight: 320
url: /es/net/aspose.words/font/shading/
---
## Font.Shading property

Devuelve un[`Shading`](../../shading/) objeto que hace referencia al formato de sombreado de la fuente.

```csharp
public Shading Shading { get; }
```

### Ejemplos

Muestra cómo aplicar sombreado al texto creado por un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Una forma de hacer visible el texto creado usando nuestro color de fuente blanco
// es aplicar un efecto de sombreado de fondo.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### Ver también

* class [Shading](../../shading/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


