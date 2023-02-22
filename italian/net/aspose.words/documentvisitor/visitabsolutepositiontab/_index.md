---
title: DocumentVisitor.VisitAbsolutePositionTab
second_title: Aspose.Words per .NET API Reference
description: DocumentVisitor metodo. Chiamato quando aAbsolutePositionTab viene rilevato un nodo nel documento.
type: docs
weight: 10
url: /it/net/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor.VisitAbsolutePositionTab method

Chiamato quando a[`AbsolutePositionTab`](../../absolutepositiontab/) viene rilevato un nodo nel documento.

```csharp
public virtual VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tab | AbsolutePositionTab | L'oggetto che viene visitato. |

### Valore di ritorno

UN[`VisitorAction`](../../visitoraction/) valore che specifica come continuare l'enumerazione.

### Esempi

Mostra come elaborare i caratteri di tabulazione della posizione assoluta con un visitatore del documento.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Estrai il contenuto testuale del nostro documento accettando questo visitatore del documento personalizzato.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // La tabulazione della posizione assoluta, che non ha equivalenti in forma di stringa, è stata convertita in modo esplicito in un carattere di tabulazione.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Anche un AbsolutePositionTab può accettare un DocumentVisitor da solo.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Raccoglie il contenuto del testo di tutte le esecuzioni nel documento visitato. Sostituisce tutti i caratteri di tabulazione assoluti con tabulazioni ordinarie.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Run nel documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo AbsolutePositionTab nel documento.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge testo all'output corrente. Rispetta il flag di uscita abilitato/disabilitato.
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
* spazio dei nomi [Aspose.Words](../../documentvisitor/)
* assemblea [Aspose.Words](../../../)


