---
title: DocumentVisitor.VisitEditableRangeEnd
second_title: Aspose.Words per .NET API Reference
description: DocumentVisitor metodo. Chiamato quando viene rilevata la fine di un intervallo modificabile nel documento.
type: docs
weight: 160
url: /it/net/aspose.words/documentvisitor/visiteditablerangeend/
---
## DocumentVisitor.VisitEditableRangeEnd method

Chiamato quando viene rilevata la fine di un intervallo modificabile nel documento.

```csharp
public virtual VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| editableRangeEnd | EditableRangeEnd | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

### Esempi

Mostra come stampare la struttura del nodo di ogni intervallo modificabile in un documento.

```csharp
public void EditableRangeToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    EditableRangeStructurePrinter visitor = new EditableRangeStructurePrinter();

    // Quando otteniamo un nodo composito per accettare un visitatore del documento, il visitatore visita il nodo di accettazione,
    // e quindi attraversa tutti i figli del nodo in modo approfondito.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario di nodi figlio di un nodo.
/// Crea una mappa sotto forma di una stringa di tutti i nodi EditableRange incontrati e dei loro figli.
/// </summary>
public class EditableRangeStructurePrinter : DocumentVisitor
{
    public EditableRangeStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideEditableRange = false;
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
        // Vogliamo stampare il contenuto delle esecuzioni, ma solo se sono all'interno di forme, come nel caso delle caselle di testo
        if (mVisitorIsInsideEditableRange) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo EditableRange nel documento.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        IndentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.Id + " Owner: " +
                            editableRangeStart.EditableRange.SingleUser);
        mDocTraversalDepth++;
        mVisitorIsInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando la visita di un nodo EditableRange è terminata.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[EditableRange end]");
        mVisitorIsInsideEditableRange = false;

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

    private bool mVisitorIsInsideEditableRange;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* enum [VisitorAction](../../visitoraction/)
* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentVisitor](../)
* spazio dei nomi [Aspose.Words](../../documentvisitor/)
* assemblea [Aspose.Words](../../../)


