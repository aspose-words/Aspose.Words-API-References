---
title: StructuredDocumentTag.ContentsFont
linktitle: ContentsFont
articleTitle: ContentsFont
second_title: Aspose.Words para .NET
description: Descubra la propiedad StructuredDocumentTag ContentsFont para un formato de texto uniforme en SDT. ¡Mejore sus documentos con opciones de fuente personalizables!
type: docs
weight: 80
url: /es/net/aspose.words.markup/structureddocumenttag/contentsfont/
---
## StructuredDocumentTag.ContentsFont property

Formato de fuente que se aplicará al texto ingresado en**TED** .

```csharp
public Font ContentsFont { get; }
```

## Ejemplos

Muestra cómo crear una etiqueta de documento estructurado en un cuadro de texto simple y modificar su apariencia.

```csharp
Document doc = new Document();

// Cree una etiqueta de documento estructurado que contendrá texto sin formato.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Establezca el título y el color del marco que aparece cuando pasa el mouse sobre la etiqueta del documento estructurado en Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Establezca una etiqueta para esta etiqueta de documento estructurado, que se puede obtener
// como un elemento XML llamado "etiqueta", con la cadena a continuación en su atributo "@val".
tag.Tag = "MyPlainTextSDT";

// Cada etiqueta de documento estructurado tiene una identificación única aleatoria.
Assert.IsTrue(tag.Id > 0);

// Establezca la fuente para el texto dentro de la etiqueta del documento estructurado.
tag.ContentsFont.Name = "Arial";

// Establezca la fuente para el texto al final de la etiqueta del documento estructurado.
// Cualquier texto que escribamos en el cuerpo del documento después de salir de la etiqueta con las teclas de flecha utilizará esta fuente.
tag.EndCharacterFont.Name = "Arial Black";

// De manera predeterminada, esto es falso y presionar Enter mientras se está dentro de una etiqueta de documento estructurado no hace nada.
// Cuando se establece como verdadero, nuestra etiqueta de documento estructurado puede tener varias líneas.

// Establezca la propiedad "Multiline" en "false" para permitir solo el contenido
// de esta etiqueta de documento estructurado para abarcar una sola línea.
// Establezca la propiedad "Multilínea" en "verdadero" para permitir que la etiqueta contenga múltiples líneas de contenido.
tag.Multiline = true;

// Establezca la propiedad "Apariencia" en "SdtAppearance.Tags" para mostrar etiquetas alrededor del contenido.
 // De forma predeterminada, la etiqueta del documento estructurado se muestra como BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Inserte un clon de nuestra etiqueta de documento estructurado en un nuevo párrafo.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Utilice el método "RemoveSelfOnly" para eliminar una etiqueta de documento estructurado, mientras conserva su contenido en el documento.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Ver también

* class [Font](../../../aspose.words/font/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
