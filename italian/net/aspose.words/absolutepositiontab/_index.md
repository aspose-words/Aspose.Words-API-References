---
title: AbsolutePositionTab
second_title: Aspose.Words per .NET API Reference
description: Una scheda di posizione assoluta è un carattere che viene utilizzato per far avanzare la posizione su la riga di testo corrente durante la visualizzazione di questo contenuto di WordprocessingML.
type: docs
weight: 10
url: /it/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

Una scheda di posizione assoluta è un carattere che viene utilizzato per far avanzare la posizione su la riga di testo corrente durante la visualizzazione di questo contenuto di WordprocessingML.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Font](../../aspose.words/inline/font) { get; } | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Restituisce vero se questo nodo può contenere altri nodi. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/specialchar/nodetype) { get; } | Restituisce **NodeType.SpecialChar** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Recupera il genitore[`Paragraph`](../paragraph) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept)(DocumentVisitor) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| override [GetText](../../aspose.words/specialchar/gettext)() | Ottiene il carattere speciale rappresentato da questo nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

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

* class [SpecialChar](../specialchar)
* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
