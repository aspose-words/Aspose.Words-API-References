---
title: Run.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words per .NET
description: Utilizza il metodo Accept per accogliere i visitatori in modo fluido, migliorando l'esperienza utente e incrementando il coinvolgimento sul tuo sito web.
type: docs
weight: 60
url: /it/net/aspose.words/run/accept/
---
## Run.Accept method

Accetta un visitatore.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore che visiterà il nodo. |

### Valore di ritorno

`falso` se il visitatore ha richiesto l'interruzione dell'enumerazione.

## Osservazioni

chiamate[`VisitRun`](../../documentvisitor/visitrun/).

Per maggiori informazioni, vedere il design pattern Visitor.

## Esempi

Mostra come stampare la struttura dei nodi di ogni intestazione e piè di pagina in un documento.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Quando otteniamo che un nodo composito accetti un visitatore del documento, il visitatore visita il nodo accettante,
    // e quindi attraversa tutti i nodi figlio in modalità depth-first.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Un modo alternativo per accedere alle intestazioni e ai piè di pagina di un documento sezione per sezione è accedere alla raccolta.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Attraversa l'albero non binario dei nodi figlio di un nodo.
/// Crea una mappa sotto forma di stringa di tutti i nodi HeaderFooter rilevati e dei loro elementi figlio.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo HeaderFooter.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che sono stati visitati tutti i nodi figlio di un nodo HeaderFooter.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiungere una riga a StringBuilder e rientrarla a seconda della profondità a cui si trova il visitatore nell'albero del documento.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* class [DocumentVisitor](../../documentvisitor/)
* class [Run](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
