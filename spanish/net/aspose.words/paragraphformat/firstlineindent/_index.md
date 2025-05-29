---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad ParagraphFormat FirstLineIndent para personalizar fácilmente las sangrías de primera línea o francesas en sus documentos para mejorar la legibilidad.
type: docs
weight: 120
url: /es/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Obtiene o establece el valor (en puntos) para una primera línea o sangría francesa.

Utilice valores positivos para establecer la sangría de primera línea y valores negativos para establecer la sangría francesa.

```csharp
public double FirstLineIndent { get; set; }
```

## Ejemplos

Muestra cómo insertar un párrafo en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// El método "Writeln" finaliza el párrafo después de agregar texto
// y luego comienza una nueva línea, agregando un nuevo párrafo.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
