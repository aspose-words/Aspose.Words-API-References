---
title: GetChildNodes
second_title: Referencia de API de Aspose.Words para .NET
description: Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado.
type: docs
weight: 100
url: /es/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| nodeType | NodeType | Especifica el tipo de nodos para seleccionar. |
| isDeep | Boolean | True para seleccionar de todos los nodos secundarios de forma recursiva. False para seleccionar solo entre los elementos secundarios inmediatos. |

### Valor_devuelto

Una colección en vivo de nodos secundarios del tipo especificado.

### Observaciones

La colección de nodos devueltos por este método siempre está activa.

Una colección en vivo siempre está sincronizada con el documento. Por ejemplo, si usted seleccionó todas las secciones en un documento y las enumera a través de la colección eliminando las secciones, la sección se elimina de la colección inmediatamente cuando se elimina del documento.

### Ejemplos

Muestra cómo imprimir todos los comentarios de un documento y sus respuestas.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Si un comentario no tiene un antepasado, es un comentario de "nivel superior" en lugar de un comentario de tipo respuesta.
// Imprime todos los comentarios de nivel superior junto con las respuestas que puedan tener.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

Muestra cómo extraer imágenes de un documento y guardarlas en el sistema de archivos local como archivos individuales.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Obtener la colección de formas del documento,
// y guarde los datos de imagen de cada forma con una imagen como un archivo en el sistema de archivos local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Los datos de imagen de las formas pueden contener imágenes de muchos formatos de imagen posibles. 
        // Podemos determinar una extensión de archivo para cada imagen automáticamente, en función de su formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Muestra cómo agregar, actualizar y eliminar nodos secundarios en la colección de elementos secundarios de CompositeNode.

```csharp
Document doc = new Document();

// Un documento vacío, por defecto, tiene un párrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Los nodos compuestos como nuestro párrafo pueden contener otros nodos compuestos y en línea como elementos secundarios.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea tres nodos de ejecución más.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// El cuerpo del documento no mostrará estas ejecuciones hasta que las insertemos en un nodo compuesto
// eso en sí mismo es parte del árbol de nodos del documento, como hicimos con la primera ejecución.
// Podemos determinar donde esta el contenido de texto de los nodos que insertamos
// aparece en el documento especificando una ubicación de inserción relativa a otro nodo en el párrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserta la segunda ejecución en el párrafo delante de la ejecución inicial.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Inserta la tercera ejecución después de la ejecución inicial.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserta la primera ejecución al comienzo de la colección de nodos secundarios del párrafo.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Podemos modificar el contenido de la ejecución editando y eliminando los nodos secundarios existentes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ver también

* class [NodeCollection](../../nodecollection)
* enum [NodeType](../../nodetype)
* class [CompositeNode](../../compositenode)
* espacio de nombres [Aspose.Words](../../compositenode)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
