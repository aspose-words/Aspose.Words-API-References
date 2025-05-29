---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ParagraphFormat LinesToDrop mejora la altura de la letra capital en sus documentos. ¡Optimice el diseño de su texto para obtener imágenes impactantes!
type: docs
weight: 210
url: /es/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Obtiene o establece el número de líneas del texto del párrafo utilizado para calcular la altura de la letra capital.

```csharp
public int LinesToDrop { get; set; }
```

## Ejemplos

Muestra cómo establecer el tamaño de una letra capital.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifique la propiedad "LinesToDrop" para designar un párrafo como letra capital,
// lo que lo convertirá en una gran letra mayúscula que decorará el siguiente párrafo.
// Asigne a esta propiedad un valor de 4 para darle a la letra capital la altura de cuatro líneas de texto.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Restablezca la propiedad "LinesToDrop" a 0 para convertir el siguiente párrafo en un párrafo normal.
//El texto de este párrafo se ajustará alrededor de la letra capital.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
