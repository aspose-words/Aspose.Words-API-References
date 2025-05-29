---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words para .NET
description: Descubra la propiedad Sombreado de fuente, que proporciona un objeto Sombreado para un formato de fuente personalizable, mejorando el atractivo visual de su texto.
type: docs
weight: 330
url: /es/net/aspose.words/font/shading/
---
## Font.Shading property

Devuelve un[`Shading`](../../shading/) objeto que hace referencia al formato de sombreado de la fuente.

```csharp
public Shading Shading { get; }
```

## Ejemplos

Muestra cómo aplicar sombreado al texto creado por un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Una forma de hacer visible el texto creado con nuestro color de fuente blanco
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
