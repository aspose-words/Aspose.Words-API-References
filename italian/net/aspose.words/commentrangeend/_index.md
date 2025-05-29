---
title: CommentRangeEnd Class
linktitle: CommentRangeEnd
articleTitle: CommentRangeEnd
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.CommentRangeEnd, che segna la fine delle aree di testo associate ai commenti. Migliora la gestione dei documenti con commenti precisi!
type: docs
weight: 440
url: /it/net/aspose.words/commentrangeend/
---
## CommentRangeEnd class

Indica la fine di una regione di testo a cui è associato un commento.

Per saperne di più, visita il[Lavorare con i commenti](https://docs.aspose.com/words/net/working-with-comments/) articolo di documentazione.

```csharp
public sealed class CommentRangeEnd : Node
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CommentRangeEnd](commentrangeend/)(*[DocumentBase](../documentbase/), int*) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Id](../../aspose.words/commentrangeend/id/) { get; set; } | Specifica l'identificatore del commento a cui è collegata questa regione. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce`VERO` se questo nodo può contenere altri nodi. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/commentrangeend/nodetype/) { get; } | RestituisceCommentRangeEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/commentrangeend/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Per creare un commento ancorato a una regione di testo, è necessario creare un[`Comment`](../comment/) and quindi crea[`CommentRangeStart`](../commentrangestart/) E`CommentRangeEnd` e impostare i loro identificatori allo stesso modo[`Id`](../comment/id/) valore.

`CommentRangeEnd` è un nodo di livello inline e può essere solo un figlio di[`Paragraph`](../paragraph/).

## Esempi

Mostra come stampare il contenuto di tutti i commenti e i relativi intervalli utilizzando un visitatore di documenti.

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

    // Aggiungi del testo al documento, inseriscilo in un intervallo di commenti e poi aggiungi il tuo commento.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Aggiungi due risposte al commento.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Esegue l'iterazione su ogni commento di primo livello e ne stampa l'intervallo, il contenuto e le risposte.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Itera su tutti i commenti di primo livello. A differenza dei commenti di tipo risposta, i commenti di primo livello non hanno antenati.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null).ToList())
    {
        // Per prima cosa, visita l'inizio dell'intervallo dei commenti.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Quindi, visita il commento e le eventuali risposte.
        comment.Accept(commentVisitor);
        // Visita solo l'inizio del commento.
        comment.AcceptStart(commentVisitor);
        // Visita solo la fine del commento.
        comment.AcceptEnd(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Infine, visita la fine dell'intervallo di commenti e quindi stampa il contenuto del testo del visitatore.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Stampa informazioni e contenuti di tutti i commenti e intervalli di commenti presenti nel documento.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Ottiene il testo normale del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo Run.
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
    /// Chiamato quando nel documento viene rilevato un nodo CommentRangeEnd.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo Commento.
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
    /// Chiamato quando la visita di un nodo Commento nel documento è terminata.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiungere una riga allo StringBuilder e rientrarla a seconda della profondità a cui si trova il visitatore nell'albero del documento.
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

* class [Node](../node/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
