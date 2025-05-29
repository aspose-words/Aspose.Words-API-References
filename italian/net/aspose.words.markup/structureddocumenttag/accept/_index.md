---
title: StructuredDocumentTag.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words per .NET
description: Scopri il metodo StructuredDocumentTag Accept: integra perfettamente le interazioni dei visitatori per migliorare le funzionalità dei documenti e il coinvolgimento degli utenti.
type: docs
weight: 330
url: /it/net/aspose.words.markup/structureddocumenttag/accept/
---
## StructuredDocumentTag.Accept method

Accetta un visitatore.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore che visiterà i nodi. |

### Valore di ritorno

Vero se tutti i nodi sono stati visitati; falso se[`DocumentVisitor`](../../../aspose.words/documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.

## Osservazioni

Enumera questo nodo e tutti i suoi figli. Ogni nodo chiama un metodo corrispondente su[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Per maggiori informazioni, vedere il design pattern Visitor.

Chiamate[`VisitStructuredDocumentTagStart`](../../../aspose.words/documentvisitor/visitstructureddocumenttagstart/) , quindi chiama[`Accept`](../../../aspose.words/node/accept/) per tutti i nodi figlio dello smart tag e delle chiamate[`VisitStructuredDocumentTagEnd`](../../../aspose.words/documentvisitor/visitstructureddocumenttagend/) alla fine.

## Esempi

Mostra come stampare la struttura del nodo di ogni tag di documento strutturato in un documento.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // Quando otteniamo che un nodo composito accetti un visitatore del documento, il visitatore visita il nodo accettante,
    // e quindi attraversa tutti i nodi figlio in modalità depth-first.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario dei nodi figlio di un nodo.
/// Crea una mappa sotto forma di stringa di tutti i nodi StructuredDocumentTag rilevati e dei relativi elementi figlio.
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
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
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo StructuredDocumentTag.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figlio di un nodo StructuredDocumentTag sono stati visitati.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

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

    private readonly bool mVisitorIsInsideStructuredDocumentTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
