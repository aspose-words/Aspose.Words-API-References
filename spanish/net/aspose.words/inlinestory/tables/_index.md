---
title: InlineStory.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words para .NET
description: Descubra las tablas InlineStory. Acceda a una colección de tablas de historias que mejoran la organización de sus datos y sus capacidades narrativas. ¡Explore ahora!
type: docs
weight: 110
url: /es/net/aspose.words/inlinestory/tables/
---
## InlineStory.Tables property

Obtiene una colección de tablas que son hijas inmediatas de la historia.

```csharp
public TableCollection Tables { get; }
```

## Ejemplos

Muestra cómo insertar nodos InlineStory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Los nodos de tabla tienen un método "EnsureMinimum()" que garantiza que la tabla tenga al menos una celda.
Table table = new Table(doc);
table.EnsureMinimum();

// Podemos colocar una tabla dentro de una nota al pie, lo que hará que aparezca en el pie de página de la página de referencia.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Una InlineStory también tiene un método "EnsureMinimum()", pero en este caso,
// se asegura de que el último hijo del nodo sea un párrafo,
// para que podamos hacer clic y escribir texto fácilmente en Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Edita la apariencia del ancla, que es el pequeño número superíndice
// en el texto principal que apunta a la nota al pie.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

//Todos los nodos de la historia en línea tienen sus respectivos tipos de historia.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Un comentario es otro tipo de historia en línea.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// El párrafo padre de un nodo de historia en línea será el del cuerpo del documento principal.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Sin embargo, el último párrafo es el del contenido del texto del comentario,
// que estará fuera del cuerpo del documento principal en una burbuja de diálogo.
// Un comentario no tendrá ningún nodo secundario de forma predeterminada,
// así que podemos aplicar el método EnsureMinimum() para colocar un párrafo aquí también.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

//Una vez que tenemos un párrafo, podemos mover el constructor para hacerlo y escribir nuestro comentario.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Ver también

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [InlineStory](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
