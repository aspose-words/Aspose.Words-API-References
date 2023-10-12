---
title: Comment.Comment
second_title: Aspose.Words per .NET API Reference
description: Comment costruttore. Inizializza una nuova istanza diComment classe.
type: docs
weight: 10
url: /it/net/aspose.words/comment/comment/
---
## Comment(DocumentBase) {#constructor}

Inizializza una nuova istanza di[`Comment`](../) classe.

```csharp
public Comment(DocumentBase doc)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |

### Osservazioni

Quando[`Comment`](../) viene creato, appartiene al documento specificato, ma non è ancora parte del documento e[`ParentNode`](../../node/parentnode/) È`nullo`.

Per aggiungere[`Comment`](../) all'uso del documentoNode) ONode) sul paragrafo in cui vuoi inserire il commento.

Dopo aver creato un commento, non dimenticare di impostarlo[`Author`](../author/) , [`Initial`](../initial/) E[`DateTime`](../datetime/) proprietà.

### Esempi

Mostra come stampare il contenuto di tutti i commenti e i relativi intervalli di commenti utilizzando un visitatore del documento.

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

    // Aggiungi testo al documento, deformalo in un intervallo di commenti, quindi aggiungi il tuo commento.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Aggiunge due risposte al commento.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Itera su ogni commento di livello superiore e stampa l'intervallo di commenti, i contenuti e le risposte.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Itera su tutti i commenti di livello superiore. A differenza dei commenti di tipo risposta, i commenti di livello superiore non hanno antenati.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // Innanzitutto, visita l'inizio dell'intervallo di commenti.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Quindi, visita il commento e le eventuali risposte che potrebbe contenere.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Infine, visita la fine dell'intervallo di commenti, quindi stampa il contenuto del testo del visitatore.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Stampa le informazioni e il contenuto di tutti i commenti e gli intervalli di commenti incontrati nel documento.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Ottiene il testo semplice del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Esegui.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo CommentRangeStart.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo CommentRangeEnd.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Commento.
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
    /// Chiamato quando la visita di un nodo Commento è terminata nel documento.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge una riga allo StringBuilder e la rientra in base alla profondità con cui si trova il visitatore nell'albero del documento.
    /// </summary>
    /// <param name="text"></param>
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

### Guarda anche

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../comment/)
* assemblea [Aspose.Words](../../../)

---

## Comment(DocumentBase, string, string, DateTime) {#constructor_1}

Inizializza una nuova istanza di[`Comment`](../) classe.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |
| author | String | Il nome dell'autore del commento. Non può essere`nullo`. |
| initial | String | L'autore sigla il commento. Non può essere`nullo`. |
| dateTime | DateTime | La data e l'ora del commento. |

### Esempi

Mostra come aggiungere un commento a un paragrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // In Microsoft Word, possiamo fare clic con il pulsante destro del mouse su questo commento nel corpo del documento per modificarlo o rispondere.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

### Guarda anche

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../comment/)
* assemblea [Aspose.Words](../../../)


