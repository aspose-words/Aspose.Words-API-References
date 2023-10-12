---
title: ParagraphFormat.LinesToDrop
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Obtiene o establece el número de líneas del texto del párrafo utilizado para calcular la altura de la letra capitular.
type: docs
weight: 210
url: /es/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Obtiene o establece el número de líneas del texto del párrafo utilizado para calcular la altura de la letra capitular.

```csharp
public int LinesToDrop { get; set; }
```

### Ejemplos

Muestra cómo establecer el tamaño de una letra capitular.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica la propiedad "LinesToDrop" para designar un párrafo como letra capitular,
// lo que lo convertirá en una gran letra mayúscula que decorará el siguiente párrafo.
// Asigne a esta propiedad un valor de 4 para darle a la letra capitular la altura de cuatro líneas de texto.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Restablece la propiedad "LinesToDrop" a 0 para convertir el siguiente párrafo en un párrafo normal.
// El texto de este párrafo se ajustará alrededor de la letra capitular.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


