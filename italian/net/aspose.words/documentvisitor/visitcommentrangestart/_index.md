---
title: DocumentVisitor.VisitCommentRangeStart
second_title: Aspose.Words per .NET API Reference
description: DocumentVisitor metodo. Chiamato quando viene rilevato linizio di un intervallo di testo commentato.
type: docs
weight: 120
url: /it/net/aspose.words/documentvisitor/visitcommentrangestart/
---
## DocumentVisitor.VisitCommentRangeStart method

Chiamato quando viene rilevato l'inizio di un intervallo di testo commentato.

```csharp
public virtual VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| commentRangeStart | CommentRangeStart | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

### Esempi

Mostra come stampare la struttura del nodo di ogni commento e intervallo di commenti in un documento.

```csharp
public void CommentsToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    CommentStructurePrinter visitor = new CommentStructurePrinter();

    // Quando otteniamo un nodo composito per accettare un visitatore del documento, il visitatore visita il nodo di accettazione,
    // e quindi attraversa tutti i figli del nodo in modo approfondito.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario di nodi figlio di un nodo.
/// Crea una mappa sotto forma di una stringa di tutti i nodi Comment/CommentRange incontrati e dei loro figli.
/// </summary>
public class CommentStructurePrinter : DocumentVisitor
{
    public CommentStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Run nel documento.
    /// Un'esecuzione viene registrata solo se è figlia di un nodo Commento o CommentRange.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo CommentRangeStart nel documento.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo CommentRangeEnd nel documento.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Commento nel documento.
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
    /// Chiamato dopo che tutti i nodi figlio di un nodo Comment sono stati visitati.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge una riga a StringBuilder e indentala a seconda della profondità del visitatore
    /// in un albero di nodi figlio di un intervallo di commenti/commenti.
    /// </summary>
    /// <nome parametro="testo"></param>
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

* enum [VisitorAction](../../visitoraction/)
* class [CommentRangeStart](../../commentrangestart/)
* class [DocumentVisitor](../)
* spazio dei nomi [Aspose.Words](../../documentvisitor/)
* assemblea [Aspose.Words](../../../)


