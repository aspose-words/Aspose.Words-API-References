---
title: DocumentVisitor.VisitFootnoteEnd
linktitle: VisitFootnoteEnd
articleTitle: VisitFootnoteEnd
second_title: Aspose.Words per .NET
description: Scopri il metodo VisitFootnoteEnd di DocumentVisitor, essenziale per gestire in modo efficiente l'enumerazione del testo delle note a piè di pagina e di chiusura nelle tue applicazioni.
type: docs
weight: 210
url: /it/net/aspose.words/documentvisitor/visitfootnoteend/
---
## DocumentVisitor.VisitFootnoteEnd method

Chiamato quando termina l'enumerazione di un testo di nota a piè di pagina o di nota di chiusura.

```csharp
public virtual VisitorAction VisitFootnoteEnd(Footnote footnote)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| footnote | Footnote | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

## Esempi

Mostra come stampare la struttura dei nodi di ogni nota a piè di pagina in un documento.

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // Quando otteniamo che un nodo composito accetti un visitatore del documento, il visitatore visita il nodo accettante,
    // e quindi attraversa tutti i nodi figlio in modalità depth-first.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario dei nodi figlio di un nodo.
/// Crea una mappa sotto forma di stringa di tutti i nodi Footnote rilevati e dei loro elementi figlio.
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// Ottiene il testo normale del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo Nota a piè di pagina.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Viene chiamato dopo che sono stati visitati tutti i nodi figlio di un nodo Nota a piè di pagina.
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiungere una riga allo StringBuilder e rientrarla a seconda della profondità a cui si trova il visitatore nell'albero del documento.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideFootnote;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* enum [VisitorAction](../../visitoraction/)
* class [Footnote](../../../aspose.words.notes/footnote/)
* class [DocumentVisitor](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
