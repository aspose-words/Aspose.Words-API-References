---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words para .NET
description: Descubre la propiedad Contorno de fuente. Formatea fácilmente las fuentes como contornos para un toque de diseño único. ¡Mejora tu tipografía con esta sencilla función!
type: docs
weight: 300
url: /es/net/aspose.words/font/outline/
---
## Font.Outline property

Verdadero si la fuente tiene el formato de contorno.

```csharp
public bool Outline { get; set; }
```

## Ejemplos

Muestra cómo crear una serie de texto con formato de esquema.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establezca la bandera Contorno para cambiar el color de relleno del texto a blanco y
 // deja un contorno fino alrededor de cada carácter en el color original del texto.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
