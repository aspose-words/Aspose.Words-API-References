---
title: DocumentVisitor Class
linktitle: DocumentVisitor
articleTitle: DocumentVisitor
second_title: Aspose.Words per .NET
description: Aspose.Words.DocumentVisitor classe. Classe base per visitatori di documenti personalizzati in C#.
type: docs
weight: 470
url: /it/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Classe base per visitatori di documenti personalizzati.

Per saperne di più, visita il[Modello oggetto documento Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public abstract class DocumentVisitor
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(*[AbsolutePositionTab](../absolutepositiontab/)*) | Chiamato quando a[`AbsolutePositionTab`](../absolutepositiontab/) è stato rilevato un nodo nel documento. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(*[Body](../body/)*) | Chiamato al termine dell'enumerazione della storia di testo principale in una sezione. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(*[Body](../body/)*) | Chiamato quando è iniziata l'enumerazione del brano di testo principale in una sezione. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(*[BookmarkEnd](../bookmarkend/)*) | Chiamato quando nel documento viene rilevata la fine di un segnalibro. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(*[BookmarkStart](../bookmarkstart/)*) | Chiamato quando nel documento viene rilevato l'inizio di un segnalibro. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | Chiamato al termine dell'enumerazione di un blocco predefinito. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | Chiamato quando è iniziata l'enumerazione di un blocco predefinito. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(*[Cell](../../aspose.words.tables/cell/)*) | Chiamato al termine dell'enumerazione di una cella di tabella. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(*[Cell](../../aspose.words.tables/cell/)*) | Chiamato quando è iniziata l'enumerazione di una cella di tabella. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(*[Comment](../comment/)*) | Chiamato al termine dell'enumerazione del testo di un commento. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(*[CommentRangeEnd](../commentrangeend/)*) | Chiamato quando viene raggiunta la fine di un intervallo di testo commentato. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(*[CommentRangeStart](../commentrangestart/)*) | Chiamato quando viene incontrato l'inizio di un intervallo di testo commentato. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(*[Comment](../comment/)*) | Chiamato quando è iniziata l'enumerazione del testo di un commento. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(*[Document](../document/)*) | Chiamato al termine dell'enumerazione del documento. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(*[Document](../document/)*) | Chiamato quando è iniziata l'enumerazione del documento. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(*[EditableRangeEnd](../editablerangeend/)*) | Chiamato quando nel documento viene rilevata la fine di un intervallo modificabile. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(*[EditableRangeStart](../editablerangestart/)*) | Chiamato quando nel documento viene rilevato l'inizio di un intervallo modificabile. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(*[FieldEnd](../../aspose.words.fields/fieldend/)*) | Chiamato quando un campo termina nel documento. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(*[FieldSeparator](../../aspose.words.fields/fieldseparator/)*) | Chiamato quando nel documento viene rilevato un separatore di campo. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(*[FieldStart](../../aspose.words.fields/fieldstart/)*) | Chiamato quando inizia un campo nel documento. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(*[Footnote](../../aspose.words.notes/footnote/)*) | Chiamato al termine dell'enumerazione del testo di una nota a piè di pagina o di chiusura. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(*[Footnote](../../aspose.words.notes/footnote/)*) | Chiamato quando è iniziata l'enumerazione del testo di una nota a piè di pagina o di chiusura. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(*[FormField](../../aspose.words.fields/formfield/)*) | Chiamato quando nel documento viene rilevato un campo modulo. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | Chiamato al termine dell'enumerazione di un documento di glossario. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | Chiamato quando è iniziata l'enumerazione di un documento di glossario. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | Chiamato al termine dell'enumerazione di una forma di gruppo. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | Chiamato quando è iniziata l'enumerazione di una forma di gruppo. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(*[HeaderFooter](../headerfooter/)*) | Chiamato al termine dell'enumerazione di un'intestazione o di un piè di pagina in una sezione. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(*[HeaderFooter](../headerfooter/)*) | Chiamato quando è iniziata l'enumerazione di un'intestazione o di un piè di pagina in una sezione. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Chiamato al termine dell'enumerazione di un oggetto Office Math. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Chiamato all'avvio dell'enumerazione di un oggetto Office Math. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(*[Paragraph](../paragraph/)*) | Chiamato al termine dell'enumerazione di un paragrafo. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(*[Paragraph](../paragraph/)*) | Chiamato quando è iniziata l'enumerazione di un paragrafo. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(*[Row](../../aspose.words.tables/row/)*) | Chiamato al termine dell'enumerazione di una riga della tabella. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(*[Row](../../aspose.words.tables/row/)*) | Chiamato quando è iniziata l'enumerazione di una riga della tabella. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(*[Run](../run/)*) | Chiamato quando viene rilevata una sequenza di testo nel file. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(*[Section](../section/)*) | Chiamato al termine dell'enumerazione di una sezione. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(*[Section](../section/)*) | Chiamato quando è iniziata l'enumerazione di una sezione. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(*[Shape](../../aspose.words.drawing/shape/)*) | Chiamato al termine dell'enumerazione di una forma. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(*[Shape](../../aspose.words.drawing/shape/)*) | Chiamato quando è iniziata l'enumerazione di una forma. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | Chiamato al termine dell'enumerazione di uno smart tag. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | Chiamato quando è iniziata l'enumerazione di uno smart tag. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(*[SpecialChar](../specialchar/)*) | Chiamato quando a[`SpecialChar`](../specialchar/) è stato rilevato un nodo nel documento. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | Chiamato al termine dell'enumerazione di un tag di documento strutturato. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(*[StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/)*) | Chiamato quando viene rilevato un StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(*[StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/)*) | Chiamato quando viene rilevato un StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | Chiamato quando è iniziata l'enumerazione di un tag di documento strutturato. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(*[SubDocument](../subdocument/)*) | Chiamato quando viene incontrato un documento secondario. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(*[Table](../../aspose.words.tables/table/)*) | Chiamato al termine dell'enumerazione di una tabella. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(*[Table](../../aspose.words.tables/table/)*) | Chiamato quando è iniziata l'enumerazione di una tabella. |

## Osservazioni

Con`DocumentVisitor` è possibile definire ed eseguire operazioni personalizzate che richiedono l'enumerazione nell'albero del documento.

Ad esempio, Aspose.Words utilizza`DocumentVisitor` internamente per il salvataggio[`Document`](../document/) in vari formati e per altre operazioni come trovare campi o segnalibri su un frammento di un documento.

Usare`DocumentVisitor`:

1. Crea una classe derivata da`DocumentVisitor`.
2. Sostituisci e fornisci implementazioni per alcuni o tutti i metodi VisitXXX per eseguire alcune operazioni personalizzate.
3. Chiamata[`Nodo.Accetta`](../node/accept/) sul[`Node`](../node/) that da cui vuoi iniziare l'enumerazione.

`DocumentVisitor` fornisce implementazioni predefinite per tutti i metodi VisitXXX per semplificare la creazione di nuovi visitatori del documento poiché è necessario sovrascrivere solo i metodi richiesti per il particolare visitatore . Non è necessario sovrascrivere tutti i metodi del visitatore.

Per ulteriori informazioni vedere il modello di progettazione Visitor.

## Esempi

Mostra come utilizzare un visitatore di documento per stampare la struttura del nodo di un documento.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Quando facciamo in modo che un nodo composito accetti un visitatore del documento, il visitatore visita il nodo accettante,
    // e poi attraversa tutti i figli del nodo in modo approfondito.
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
    /// Chiamato quando viene incontrato un nodo Documento.
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
    /// Chiamato dopo che tutti i nodi figli di un nodo Documento sono stati visitati.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Sezione.
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
    /// Chiamato dopo che tutti i nodi figli di un nodo Sezione sono stati visitati.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Body.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figli di un nodo Body sono stati visitati.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Paragrafo.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato dopo che tutti i nodi figli di un nodo Paragrafo sono stati visitati.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Esegui.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo Sottodocumento.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Aggiunge una riga allo StringBuilder e la rientra in base alla profondità con cui si trova il visitatore nell'albero del documento.
    /// </summary>
    /// <param name="text"></param>
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
