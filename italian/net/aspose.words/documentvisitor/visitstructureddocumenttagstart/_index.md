---
title: DocumentVisitor.VisitStructuredDocumentTagStart
second_title: Aspose.Words per .NET API Reference
description: DocumentVisitor metodo. Chiamato quando è iniziata lenumerazione di un tag di documento strutturato.
type: docs
weight: 470
url: /it/net/aspose.words/documentvisitor/visitstructureddocumenttagstart/
---
## DocumentVisitor.VisitStructuredDocumentTagStart method

Chiamato quando è iniziata l'enumerazione di un tag di documento strutturato.

```csharp
public virtual VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdt | StructuredDocumentTag | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

### Esempi

Mostra come stampare la struttura del nodo di ogni tag di documento strutturato in un documento.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // Quando otteniamo un nodo composito per accettare un visitatore del documento, il visitatore visita il nodo di accettazione,
    // e quindi attraversa tutti i figli del nodo in modo approfondito.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario di nodi figlio di un nodo.
/// Crea una mappa sotto forma di una stringa di tutti i nodi StructuredDocumentTag incontrati e dei loro figli.
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
    /// Chiamato quando viene rilevato un nodo Run nel documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo StructuredDocumentTag nel documento.
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
    /// Aggiunge una riga a StringBuilder e la indenta in base alla profondità del visitatore nell'albero del documento.
    /// </summary>
    /// <nome parametro="testo"></param>
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

* enum [VisitorAction](../../visitoraction/)
* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentVisitor](../)
* spazio dei nomi [Aspose.Words](../../documentvisitor/)
* assemblea [Aspose.Words](../../../)


