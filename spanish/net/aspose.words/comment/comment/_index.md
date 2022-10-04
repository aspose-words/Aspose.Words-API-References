---
title: Comment
second_title: Referencia de API de Aspose.Words para .NET
description: Inicializa una nueva instancia del Comentario clase.
type: docs
weight: 10
url: /es/net/aspose.words/comment/comment/
---
## Comment(DocumentBase) {#constructor}

Inicializa una nueva instancia del **Comentario** clase.

```csharp
public Comment(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

### Observaciones

Cuando **Comentario** se crea, pertenece al documento especificado, pero aún no es parte del documento y **Nodo principal** es nulo.

Para anexar **Comentario** al documento use InsertAfter o InsertBefore en el párrafo donde desea insertar el comentario.

Después de crear un comentario, no olvide configurar su[`Author`](../author/) , [`Initial`](../initial/) y[`DateTime`](../datetime/) propiedades.

### Ejemplos

Muestra cómo imprimir el contenido de todos los comentarios y sus rangos de comentarios utilizando un visitante del documento.

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

    // Agregue texto al documento, deformelo en un rango de comentarios y luego agregue su comentario.
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
/// Itera sobre cada comentario de nivel superior e imprime su rango de comentarios, contenido y respuestas.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Iterar sobre todos los comentarios de nivel superior. A diferencia de los comentarios de tipo respuesta, los comentarios de nivel superior no tienen un antepasado.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // Primero, visita el inicio del rango de comentarios.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Luego, visita el comentario y cualquier respuesta que pueda tener.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Finalmente, visite el final del rango de comentarios y luego imprima el contenido de texto del visitante.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Imprime información y contenido de todos los comentarios y rangos de comentarios encontrados en el documento.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo CommentRangeStart en el documento.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo CommentRangeEnd en el documento.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Comentario en el documento.
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
    /// Se llama cuando finaliza la visita de un nodo de comentario en el documento.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agregue una línea al StringBuilder y sangre dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <parámetro nombre="texto"></parámetro>
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

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* espacio de nombres [Aspose.Words](../../comment/)
* asamblea [Aspose.Words](../../../)

---

## Comment(DocumentBase, string, string, DateTime) {#constructor_1}

Inicializa una nueva instancia del **Comentario** clase.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| author | String | El nombre del autor del comentario. No puede ser nulo. |
| initial | String | Las iniciales del autor para el comentario. No puede ser nulo. |
| dateTime | DateTime | La fecha y la hora del comentario. |

### Ejemplos

Muestra cómo agregar un comentario a un párrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// En Microsoft Word, podemos hacer clic derecho en este comentario en el cuerpo del documento para editarlo o responderlo. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

### Ver también

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* espacio de nombres [Aspose.Words](../../comment/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
