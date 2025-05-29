---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words para .NET
description: Descubra la propiedad ParagraphFormat OutlineLevel para definir fácilmente la jerarquía de párrafos en sus documentos, mejorando la organización y la legibilidad.
type: docs
weight: 260
url: /es/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Especifica el nivel de esquema del párrafo en el documento.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Ejemplos

Muestra cómo configurar los niveles de esquema de párrafo para crear texto contraíble.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada párrafo tiene un OutlineLevel, que puede ser cualquier número del 1 al 9, o el valor predeterminado "BodyText".
// Al establecer la propiedad en uno de los valores numerados se mostrará una flecha hacia la izquierda
// del inicio del párrafo.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// El nivel 1 es el más alto. Si hay un párrafo de nivel inferior debajo de otro de nivel superior,
// Al contraer el párrafo de nivel superior se contraerá el párrafo de nivel inferior.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Dos párrafos del mismo nivel no se colapsarán entre sí,
// y las flechas no colapsan los párrafos a los que apuntan.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// El valor predeterminado de "BodyText" es el más bajo que puede contraer un párrafo de cualquier nivel.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Ver también

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
