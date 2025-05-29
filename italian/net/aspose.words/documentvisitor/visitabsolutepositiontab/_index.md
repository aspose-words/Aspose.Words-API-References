---
title: DocumentVisitor.VisitAbsolutePositionTab
linktitle: VisitAbsolutePositionTab
articleTitle: VisitAbsolutePositionTab
second_title: Aspose.Words per .NET
description: Scopri il metodo VisitAbsolutePositionTab di DocumentVisitor, progettato per migliorare l'elaborazione dei documenti gestendo in modo efficiente i nodi AbsolutePositionTab.
type: docs
weight: 10
url: /it/net/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor.VisitAbsolutePositionTab method

Chiamato quando un[`AbsolutePositionTab`](../../absolutepositiontab/) il nodo è stato riscontrato nel documento.

```csharp
public virtual VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tab | AbsolutePositionTab | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

## Esempi

Mostra come elaborare i caratteri di tabulazione in posizione assoluta con un visitatore del documento.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Estrarre il contenuto di testo del nostro documento accettando questo visitatore del documento personalizzato.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Visita solo l'inizio del corpo del documento.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Visita solo la fine del corpo del documento.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // La posizione assoluta tab, che non ha equivalenti in formato stringa, è stata convertita esplicitamente in un carattere di tabulazione.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Anche un AbsolutePositionTab può accettare autonomamente un DocumentVisitor.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Raccoglie il contenuto testuale di tutte le esecuzioni nel documento visitato. Sostituisce tutti i caratteri di tabulazione assoluti con tabulazioni normali.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo AbsolutePositionTab.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge testo all'output corrente. Rispetta il flag di output abilitato/disabilitato.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Testo normale del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* enum [VisitorAction](../../visitoraction/)
* class [AbsolutePositionTab](../../absolutepositiontab/)
* class [DocumentVisitor](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
