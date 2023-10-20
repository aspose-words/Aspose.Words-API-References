---
title: StructuredDocumentTag.Level
linktitle: Level
articleTitle: Level
second_title: Aspose.Words para .NET
description: StructuredDocumentTag Level propiedad. Obtiene el nivel en el que esteTED ocurre en el árbol del documento en C#.
type: docs
weight: 170
url: /es/net/aspose.words.markup/structureddocumenttag/level/
---
## StructuredDocumentTag.Level property

Obtiene el nivel en el que este**TED** ocurre en el árbol del documento.

```csharp
public MarkupLevel Level { get; }
```

## Ejemplos

Muestra cómo crear una etiqueta de documento estructurado en un cuadro de texto sin formato y modificar su apariencia.

```csharp
Document doc = new Document();

// Crea una etiqueta de documento estructurado que contendrá texto sin formato.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Establece el título y el color del marco que aparece cuando pasas el mouse sobre la etiqueta del documento estructurado en Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Establece una etiqueta para esta etiqueta de documento estructurado, que se puede obtener
// como un elemento XML denominado "etiqueta", con la cadena siguiente en su atributo "@val".
tag.Tag = "MyPlainTextSDT";

// Cada etiqueta de documento estructurado tiene una identificación única aleatoria.
Assert.That(tag.Id, Is.Positive);

// Establece la fuente para el texto dentro de la etiqueta del documento estructurado.
tag.ContentsFont.Name = "Arial";

// Establece la fuente para el texto al final de la etiqueta del documento estructurado.
// Cualquier texto que escribamos en el cuerpo del documento después de salir de la etiqueta con las teclas de flecha utilizará esta fuente.
tag.EndCharacterFont.Name = "Arial Black";

// De forma predeterminada, esto es falso y presionar Intro mientras se encuentra dentro de una etiqueta de documento estructurado no hace nada.
// Cuando se establece en verdadero, nuestra etiqueta de documento estructurado puede tener varias líneas.

// Establece la propiedad "Multilínea" en "falso" para permitir solo el contenido
// de esta etiqueta de documento estructurado para abarcar una sola línea.
// Establece la propiedad "Multiline" en "true" para permitir que la etiqueta contenga varias líneas de contenido.
tag.Multiline = true;

// Establece la propiedad "Apariencia" en "SdtAppearance.Tags" para mostrar etiquetas alrededor del contenido.
 // De forma predeterminada, la etiqueta del documento estructurado se muestra como BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Inserta un clon de nuestra etiqueta de documento estructurado en un nuevo párrafo.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Utilice el método "RemoveSelfOnly" para eliminar una etiqueta de documento estructurado, manteniendo su contenido en el documento.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Ver también

* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
