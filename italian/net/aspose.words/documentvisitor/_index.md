---
title: DocumentVisitor
second_title: Aspose.Words per .NET API Reference
description: Classe base per visitatori di documenti personalizzati.
type: docs
weight: 460
url: /it/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Classe base per visitatori di documenti personalizzati.

```csharp
public abstract class DocumentVisitor
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(AbsolutePositionTab) | Chiamato quando a[`AbsolutePositionTab`](../absolutepositiontab/) viene rilevato un nodo nel documento. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(Body) | Chiamato quando l'enumerazione della storia di testo principale in una sezione è terminata. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(Body) | Chiamato quando è iniziata l'enumerazione della storia di testo principale in una sezione. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(BookmarkEnd) | Chiamato quando viene rilevata la fine di un segnalibro nel documento. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(BookmarkStart) | Chiamato quando viene rilevato l'inizio di un segnalibro nel documento. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(BuildingBlock) | Chiamato al termine dell'enumerazione di un building block. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(BuildingBlock) | Chiamato quando è iniziata l'enumerazione di un building block. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(Cell) | Chiamato quando l'enumerazione di una cella di tabella è terminata. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(Cell) | Chiamato quando è iniziata l'enumerazione di una cella di tabella. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(Comment) | Chiamato quando l'enumerazione di un testo di commento è terminata. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(CommentRangeEnd) | Chiamato quando viene rilevata la fine di un intervallo di testo commentato. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(CommentRangeStart) | Chiamato quando viene rilevato l'inizio di un intervallo di testo commentato. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(Comment) | Chiamato quando è iniziata l'enumerazione di un testo di commento. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(Document) | Chiamato al termine dell'enumerazione del documento. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(Document) | Chiamato quando è iniziata l'enumerazione del documento. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(EditableRangeEnd) | Chiamato quando viene rilevata la fine di un intervallo modificabile nel documento. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(EditableRangeStart) | Chiamato quando viene rilevato l'inizio di un intervallo modificabile nel documento. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(FieldEnd) | Chiamato quando un campo termina nel documento. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(FieldSeparator) | Chiamato quando viene rilevato un separatore di campo nel documento. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(FieldStart) | Chiamato quando un campo inizia nel documento. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(Footnote) | Chiamato quando l'enumerazione di una nota a piè di pagina o del testo di una nota di chiusura è terminata. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(Footnote) | Chiamato quando è iniziata l'enumerazione di una nota a piè di pagina o del testo di una nota di chiusura. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(FormField) | Chiamato quando viene rilevato un campo modulo nel documento. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(GlossaryDocument) | Chiamato quando l'enumerazione di un documento del glossario è terminata. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(GlossaryDocument) | Chiamato quando è iniziata l'enumerazione di un documento del glossario. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(GroupShape) | Chiamato quando l'enumerazione di una forma di gruppo è terminata. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(GroupShape) | Chiamato quando è iniziata l'enumerazione di una forma di gruppo. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(HeaderFooter) | Chiamato quando l'enumerazione di un'intestazione o di un piè di pagina in una sezione è terminata. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(HeaderFooter) | Chiamato quando è iniziata l'enumerazione di un'intestazione o di un piè di pagina in una sezione. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(OfficeMath) | Chiamato al termine dell'enumerazione di un oggetto Office Math. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(OfficeMath) | Chiamato all'avvio dell'enumerazione di un oggetto Office Math. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(Paragraph) | Chiamato quando l'enumerazione di un paragrafo è terminata. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(Paragraph) | Chiamato quando è iniziata l'enumerazione di un paragrafo. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(Row) | Chiamato quando l'enumerazione di una riga di tabella è terminata. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(Row) | Chiamato quando è iniziata l'enumerazione di una riga di tabella. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(Run) | Chiamato quando viene rilevata una sequenza di testo in. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(Section) | Chiamato quando l'enumerazione di una sezione è terminata. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(Section) | Chiamato quando è iniziata l'enumerazione di una sezione. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(Shape) | Chiamato quando l'enumerazione di una forma è terminata. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(Shape) | Chiamato quando è iniziata l'enumerazione di una forma. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(SmartTag) | Chiamato al termine dell'enumerazione di uno smart tag. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(SmartTag) | Chiamato quando è iniziata l'enumerazione di uno smart tag. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(SpecialChar) | Chiamato quando a[`SpecialChar`](../specialchar/) viene rilevato un nodo nel documento. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(StructuredDocumentTag) | Chiamato al termine dell'enumerazione di un tag di documento strutturato. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(StructuredDocumentTag) | Chiamato quando è iniziata l'enumerazione di un tag di documento strutturato. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(SubDocument) | Chiamato quando viene rilevato un documento secondario. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(Table) | Chiamato quando l'enumerazione di una tabella è terminata. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(Table) | Chiamato quando è iniziata l'enumerazione di una tabella. |

### Osservazioni

Insieme a **DocumentVisitor** è possibile definire ed eseguire operazioni personalizzate che richiedono l'enumerazione nell'albero del documento.

Ad esempio, utilizza Aspose.Words **DocumentVisitor** internamente per il risparmio **Documento** in vari formati e per altre operazioni come trovare campi o segnalibri su un frammento di un documento.

Usare **DocumentVisitor**:

1. Crea una classe derivata da **DocumentVisitor**.
2. Eseguire l'override e fornire implementazioni per alcuni o tutti i metodi VisitXXX per eseguire alcune operazioni personalizzate.
3. Chiamata[`Nodo.Accetta`](../node/accept/) sul **Nodo** quel da cui vuoi iniziare l'enumerazione.

**DocumentVisitor**fornisce implementazioni predefinite per tutti i metodi VisitXXX per semplificare la creazione di nuovi visitatori di documenti poiché solo i metodi richiesti per il particolare visitatore devono essere sovrascritti. Non è necessario sovrascrivere tutti i metodi del visitatore.

Per ulteriori informazioni, vedere il modello di progettazione del visitatore.

### Esempi

Mostra come utilizzare un visitatore del documento per stampare la struttura del nodo di un documento.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Quando otteniamo un nodo composito per accettare un visitatore del documento, il visitatore visita il nodo di accettazione,
    // e quindi attraversa tutti i figli del nodo in modo approfondito.
    // Il visitatore può leggere e modificare ogni nodo visitato.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Attraversa l'albero dei nodi figli di un nodo.
/// Crea una mappa di questo albero sotto forma di stringa.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Document.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Consenti al visitatore di continuare a visitare altri nodi.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figlio di un nodo Document sono stati visitati.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Sezione nel documento.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Ottieni l'indice della nostra sezione all'interno del documento.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figlio di un nodo Sezione sono stati visitati.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Body nel documento.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figlio di un nodo Body sono stati visitati.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando si incontra un nodo Paragrafo nel documento.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figlio di un nodo Paragraph sono stati visitati.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo Run nel documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo SubDocument nel documento.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge una riga a StringBuilder e la indenta in base alla profondità del visitatore nell'albero del documento.
    /// </summary>
    /// <nome parametro="testo"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
