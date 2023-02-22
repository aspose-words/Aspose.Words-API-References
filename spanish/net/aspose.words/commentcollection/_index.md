---
title: Class CommentCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.CommentCollection clase. Proporciona acceso escrito a una colección deComment nodos.
type: docs
weight: 230
url: /es/net/aspose.words/commentcollection/
---
## CommentCollection class

Proporciona acceso escrito a una colección de[`Comment`](../comment/) nodos.

```csharp
public class CommentCollection : NodeCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtiene el número de nodos de la colección. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Recupera un **Comentario** en el índice dado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Determina si un nodo está en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Proporciona una iteración de estilo "foreach" simple sobre la colección de nodos. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Devuelve el índice de base cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Inserta un nodo en la colección en el índice especificado. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copia todos los nodos de la colección a una nueva matriz de nodos. |

### Ejemplos

Muestra cómo marcar un comentario como "hecho".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

// Inserta un comentario para señalar un error. 
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

// Los comentarios tienen un indicador "Terminado", que se establece en "falso" de forma predeterminada. 
// Si un comentario sugiere que hagamos un cambio dentro del documento,
// podemos aplicar el cambio y luego también establecer el indicador "Listo" para indicar la corrección.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Los comentarios que están "hechos" se diferenciarán
// de los que no están "terminados" con un color de texto descolorido.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Ver también

* class [NodeCollection](../nodecollection/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


