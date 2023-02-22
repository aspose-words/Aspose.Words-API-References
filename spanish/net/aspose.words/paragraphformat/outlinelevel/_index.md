---
title: ParagraphFormat.OutlineLevel
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Especifica el nivel de esquema del párrafo en el documento.
type: docs
weight: 240
url: /es/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Especifica el nivel de esquema del párrafo en el documento.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

### Ejemplos

Muestra cómo configurar niveles de esquema de párrafo para crear texto contraíble.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada párrafo tiene un nivel de contorno, que puede ser cualquier número del 1 al 9, o el valor predeterminado "BodyText".
// Establecer la propiedad en uno de los valores numerados mostrará una flecha a la izquierda
// del principio del párrafo.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// El nivel 1 es el nivel superior. Si hay un párrafo con un nivel inferior debajo de un párrafo con un nivel superior,
// colapsar el párrafo de nivel superior colapsará el párrafo de nivel inferior.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Dos párrafos del mismo nivel no colapsarán entre sí,
// y las flechas no colapsan los párrafos a los que apuntan.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// El valor predeterminado de "BodyText" es el más bajo, que un párrafo de cualquier nivel puede colapsar.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Ver también

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


