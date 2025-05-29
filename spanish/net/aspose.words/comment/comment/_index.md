---
title: Comment
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words para .NET
description: Crea comentarios atractivos fácilmente con nuestro constructor de comentarios. Inicializa una nueva instancia de la clase Comentario y mejora la interacción del usuario sin problemas.
type: docs
weight: 10
url: /es/net/aspose.words/comment/comment/
---
## Comment(*[DocumentBase](../../documentbase/)*) {#constructor}

Inicializa una nueva instancia del[`Comment`](../) clase.

```csharp
public Comment(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

## Observaciones

Cuando[`Comment`](../) se crea, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../node/parentnode/) es`nulo`.

Para anexar[`Comment`](../) al uso del documento[`InsertAfter`](../../compositenode/insertafter/) o[`InsertBefore`](../../compositenode/insertbefore/) en el párrafo donde desea insertar el comentario.

Después de crear un comentario, no olvides configurarlo[`Author`](../author/) , [`Initial`](../initial/) y[`DateTime`](../datetime/) propiedades.

## Ejemplos

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

    // Agregue texto al documento, deformelo en un rango de comentarios y luego agregue su comentario.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    //Añadir dos respuestas al comentario.
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

    // Itera sobre todos los comentarios de nivel superior. A diferencia de los comentarios de tipo respuesta, los comentarios de nivel superior no tienen antecesor.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null).ToList())
    {
        // Primero, visita el inicio del rango de comentarios.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Luego, visita el comentario y cualquier respuesta que pueda tener.
        comment.Accept(commentVisitor);
        // Visita solo el inicio del comentario.
        comment.AcceptStart(commentVisitor);
        // Visita solo el final del comentario.
        comment.AcceptEnd(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Finalmente, visite el final del rango de comentarios y luego imprima el contenido del texto del visitante.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Imprime información y el contenido de todos los comentarios y rangos de comentarios encontrados en el documento.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Obtiene el texto simple del documento que fue acumulado por el visitante.
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
    /// Se llama cuando finaliza la visita a un nodo Comentario en el documento.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangrala dependiendo de qué tan profundo se encuentre el visitante en el árbol del documento.
    /// </summary>
    /// <param name="texto"></param>
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Comment(*[DocumentBase](../../documentbase/), string, string, DateTime*) {#constructor_1}

Inicializa una nueva instancia del[`Comment`](../) clase.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| author | String | El nombre del autor del comentario. No puede ser`nulo`. |
| initial | String | Las iniciales del autor para el comentario. No se puede`nulo`. |
| dateTime | DateTime | La fecha y hora del comentario. |

## Ejemplos

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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
