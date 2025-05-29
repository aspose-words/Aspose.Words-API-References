---
title: Body.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words per .NET
description: Scopri il metodo Body AcceptStart per integrare perfettamente i visitatori all'inizio del corpo del tuo documento, migliorando l'esperienza utente.
type: docs
weight: 60
url: /it/net/aspose.words/body/acceptstart/
---
## Body.AcceptStart method

Accetta un visitatore per visitare l'inizio del corpo del documento.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore del documento. |

### Valore di ritorno

L'azione che il visitatore deve intraprendere.

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
* class [DocumentVisitor](../../documentvisitor/)
* class [Body](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
