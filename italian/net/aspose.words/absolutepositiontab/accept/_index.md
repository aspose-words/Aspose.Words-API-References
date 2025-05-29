---
title: AbsolutePositionTab.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words per .NET
description: Scopri il metodo AbsolutePositionTab Accept per un coinvolgimento fluido dei visitatori. Migliora l'interattività del tuo sito e aumenta la soddisfazione degli utenti oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab.Accept method

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

chiamate[`VisitAbsolutePositionTab`](../../documentvisitor/visitabsolutepositiontab/).

Per maggiori informazioni, vedere il design pattern Visitor.

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

* class [DocumentVisitor](../../documentvisitor/)
* class [AbsolutePositionTab](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
