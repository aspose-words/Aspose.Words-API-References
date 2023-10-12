---
title: Class CommentRangeStart
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.CommentRangeStart clase. Indica el inicio de una región de texto que tiene un comentario asociado.
type: docs
weight: 260
url: /es/net/aspose.words/commentrangestart/
---
## CommentRangeStart class

Indica el inicio de una región de texto que tiene un comentario asociado.

Para obtener más información, visite el[Trabajar con comentarios](https://docs.aspose.com/words/net/working-with-comments/) artículo de documentación.

```csharp
public sealed class CommentRangeStart : Node
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CommentRangeStart](commentrangestart/)(DocumentBase, int) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Id](../../aspose.words/commentrangestart/id/) { get; set; } | Especifica el identificador del comentario al que está vinculada esta región. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devoluciones`verdadero` si este nodo puede contener otros nodos. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/commentrangestart/nodetype/) { get; } | DevolucionesCommentRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/) objeto que representa la parte de un documento contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/commentrangestart/accept/)(DocumentVisitor) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer antepasado del tipo de objeto especificado. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

### Observaciones

Para crear un comentario anclado a una región de texto, necesita crear un[`Comment`](../comment/) and luego crea`CommentRangeStart` y[`CommentRangeEnd`](../commentrangeend/) establecer sus identificadores al mismo[`Id`](../comment/id/) valor.

`CommentRangeStart` es un nodo de nivel en línea y sólo puede ser hijo de[`Paragraph`](../paragraph/).

### Ejemplos

Muestra cómo imprimir el contenido de todos los comentarios y sus rangos de comentarios utilizando un visitante de documentos.

```csharp
public void CreateCommentsAndPrintAllInfo()
{
    Document doc = new Document();

    Comment newComment = new Comment(doc)
    {
        Author = "VDeryushev",
        Initial = "VD",
        DateTime = DateTime.Now
    };

    newComment.SetText("Comment regarding text.");

    // Agrega texto al documento, deformalo en un rango de comentarios y luego agrega tu comentario.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Agrega dos respuestas al comentario.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Itera sobre cada comentario de nivel superior e imprime su rango de comentarios, contenidos y respuestas.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Iterar sobre todos los comentarios de nivel superior. A diferencia de los comentarios de tipo respuesta, los comentarios de nivel superior no tienen antepasados.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // Primero, visita el inicio del rango de comentarios.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Luego, visita el comentario y las respuestas que pueda tener.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Finalmente, visite el final del rango de comentarios y luego imprima el contenido del texto del visitante.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Imprime la información y el contenido de todos los comentarios y rangos de comentarios encontrados en el documento.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo CommentRangeStart en el documento.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo CommentRangeEnd en el documento.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Comentario en el documento.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        IndentAndAppendLine(
            $"[Comment start] For comment range ID {comment.Id}, By {comment.Author} on {comment.DateTime}");
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando finaliza la visita de un nodo Comentario en el documento.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangra dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <param nombre="texto"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideComment;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


