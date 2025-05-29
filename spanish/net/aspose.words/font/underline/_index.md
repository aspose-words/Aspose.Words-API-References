---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words para .NET
description: Descubre la propiedad Subrayado de fuente para personalizar los estilos de texto. Configura y modifica fácilmente los tipos de subrayado para mejorar la tipografía de tus diseños.
type: docs
weight: 540
url: /es/net/aspose.words/font/underline/
---
## Font.Underline property

Obtiene o establece el tipo de subrayado aplicado a la fuente.

```csharp
public Underline Underline { get; set; }
```

## Ejemplos

Muestra cómo configurar el estilo y el color de un subrayado de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

Muestra cómo insertar texto formateado utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifique el formato de fuente y luego agregue texto.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Muestra cómo insertar un campo de hipervínculo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto en el que se puede hacer clic y que nos llevará a la ubicación especificada en la URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falso);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL a través de una nueva ventana del navegador web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Ver también

* enum [Underline](../../underline/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
