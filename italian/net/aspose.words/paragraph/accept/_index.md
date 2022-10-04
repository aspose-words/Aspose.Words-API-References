---
title: Accept
second_title: Aspose.Words per .NET API Reference
description: Accetta un visitatore.
type: docs
weight: 230
url: /it/net/aspose.words/paragraph/accept/
---
## Paragraph.Accept method

Accetta un visitatore.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore che visiterà i nodi. |

### Valore di ritorno

Vero se tutti i nodi sono stati visitati; false se DocumentVisitor ha interrotto l'operazione prima di visitare tutti i nodi.

### Osservazioni

Enumera su questo nodo e tutti i suoi figli. Ogni nodo chiama un metodo corrispondente su DocumentVisitor.

Per ulteriori informazioni, vedere il modello di progettazione del visitatore.

Chiama DocumentVisitor.VisitParagraphStart, quindi chiama Accept per tutti i nodi figlio del paragrafo e chiama DocumentVisitor.VisitParagraphEnd alla fine.

### Esempi

Mostra come utilizzare un'implementazione di DocumentVisitor per rimuovere tutto il contenuto nascosto da un documento.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Di seguito sono riportati tre tipi di campi che possono accettare un visitatore del documento,
    // che gli consentirà di visitare il nodo di accettazione e quindi di attraversare i suoi nodi figli in modo approfondito.
    // 1 - Nodo paragrafo:
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Nodo tabella:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Nodo documento:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

/// <summary>
/// Rimuove tutti i nodi visitati contrassegnati come "contenuto nascosto".
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Chiamato quando viene rilevato un nodo FieldStart nel documento.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo FieldEnd nel documento.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo FieldSeparator nel documento.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Run nel documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando si incontra un nodo Paragrafo nel documento.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un FormField nel documento.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un GroupShape nel documento.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevata una forma nel documento.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un commento nel documento.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevata una nota a piè di pagina nel documento.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato uno SpecialCharacter nel documento.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando la visita di un nodo Tabella è terminata nel documento.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Il contenuto all'interno delle celle della tabella potrebbe avere il flag del contenuto nascosto, ma le tabelle stesse no.
        // Se questa tabella non avesse altro che contenuto nascosto, questo visitatore lo avrebbe rimosso tutto,
        // e non ci sarebbero più nodi figli.
        // Pertanto, possiamo anche trattare la tabella stessa come contenuto nascosto e rimuoverla.
        // Le tabelle vuote ma senza contenuto nascosto avranno celle con paragrafi vuoti all'interno,
        // che questo visitatore non rimuoverà.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando la visita di un nodo Cell è terminata nel documento.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando la visita di un nodo Riga è terminata nel documento.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Guarda anche

* class [DocumentVisitor](../../documentvisitor/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
