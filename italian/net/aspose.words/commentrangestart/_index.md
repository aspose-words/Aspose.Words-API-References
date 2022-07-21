---
title: CommentRangeStart
second_title: Aspose.Words per .NET API Reference
description: Indica linizio di unarea di testo a cui è associato un commento.
type: docs
weight: 250
url: /it/net/aspose.words/commentrangestart/
---
## CommentRangeStart class

Indica l'inizio di un'area di testo a cui è associato un commento.

```csharp
public sealed class CommentRangeStart : Node
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CommentRangeStart](commentrangestart)(DocumentBase, int) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Id](../../aspose.words/commentrangestart/id) { get; set; } | Specifica l'identificatore del commento a cui è collegata questa regione. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Restituisce vero se questo nodo può contenere altri nodi. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/commentrangestart/nodetype) { get; } | RestituisceCommentRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/commentrangestart/accept)(DocumentVisitor) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| virtual [GetText](../../aspose.words/node/gettext)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

Per creare un commento ancorato a un'area di testo, è necessario creare un[`Comment`](../comment) e quindi crea[`CommentRangeStart`](../commentrangestart) e[`CommentRangeEnd`](../commentrangeend) imposta i loro identificatori sullo stesso[`Id`](../comment/id) valore.

[`CommentRangeStart`](../commentrangestart) è un nodo inline e può essere solo un figlio di[`Paragraph`](../paragraph).

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

    // Aggiungi due risposte al commento.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Esegue l'iterazione su ogni commento di primo livello e ne stampa l'intervallo di commenti, i contenuti e le risposte.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Itera su tutti i commenti di primo livello. A differenza dei commenti di tipo risposta, i commenti di primo livello non hanno predecessori.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // Per prima cosa, visita l'inizio dell'intervallo di commenti.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Quindi, visita il commento e tutte le risposte che potrebbe avere.
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
    /// Ottiene il testo normale del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Run nel documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

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
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
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
    /// Aggiunge una riga a StringBuilder e la indenta in base alla profondità del visitatore nell'albero del documento.
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

* class [Node](../node)
* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
