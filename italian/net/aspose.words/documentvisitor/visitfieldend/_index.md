---
title: DocumentVisitor.VisitFieldEnd
linktitle: VisitFieldEnd
articleTitle: VisitFieldEnd
second_title: Aspose.Words per .NET
description: Scopri il metodo VisitFieldEnd di DocumentVisitor, essenziale per gestire la terminazione dei campi nei documenti. Migliora subito la tua efficienza di programmazione!
type: docs
weight: 180
url: /it/net/aspose.words/documentvisitor/visitfieldend/
---
## DocumentVisitor.VisitFieldEnd method

Chiamato quando un campo termina nel documento.

```csharp
public virtual VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldEnd | FieldEnd | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

## Osservazioni

Per maggiori informazioni vedere[`VisitFieldStart`](../visitfieldstart/)

## Esempi

Mostra come stampare la struttura dei nodi di ogni campo in un documento.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // Quando otteniamo che un nodo composito accetti un visitatore del documento, il visitatore visita il nodo accettante,
    // e quindi attraversa tutti i nodi figlio in modalità depth-first.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero non binario dei nodi figlio di un nodo.
/// Crea una mappa sotto forma di stringa di tutti i nodi Field rilevati e dei loro figli.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
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
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldEnd.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiungi una riga allo StringBuilder e rientrala a seconda della profondità del visitatore
    /// nell'albero dei nodi figlio del campo.
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

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* enum [VisitorAction](../../visitoraction/)
* class [FieldEnd](../../../aspose.words.fields/fieldend/)
* class [DocumentVisitor](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
