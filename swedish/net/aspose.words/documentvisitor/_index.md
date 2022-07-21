---
title: DocumentVisitor
second_title: Aspose.Words för .NET API Referens
description: Basklass för anpassade dokumentbesökare.
type: docs
weight: 460
url: /sv/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Basklass för anpassade dokumentbesökare.

```csharp
public abstract class DocumentVisitor
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab)(AbsolutePositionTab) | Ringde när en[`AbsolutePositionTab`](../absolutepositiontab) nod påträffas i dokumentet. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend)(Body) | Anropas när uppräkningen av huvudtextberättelsen i ett avsnitt har avslutats. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart)(Body) | Anropas när uppräkningen av huvudtextberättelsen i ett avsnitt har börjat. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend)(BookmarkEnd) | Anropas när slutet av ett bokmärke påträffas i dokumentet. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart)(BookmarkStart) | Anropas när en början av ett bokmärke påträffas i dokumentet. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend)(BuildingBlock) | Anropas när uppräkningen av ett byggblock har avslutats. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart)(BuildingBlock) | Anropas när uppräkningen av ett byggblock har påbörjats. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend)(Cell) | Anropas när uppräkningen av en tabellcell har avslutats. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart)(Cell) | Anropas när uppräkningen av en tabellcell har startat. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend)(Comment) | Anropas när uppräkningen av en kommentarstext har avslutats. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend)(CommentRangeEnd) | Anropas när slutet av ett kommenterat textintervall påträffas. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart)(CommentRangeStart) | Anropas när början av ett kommenterat textintervall påträffas. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart)(Comment) | Anropas när uppräkningen av en kommentarstext har börjat. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend)(Document) | Anropas när uppräkningen av dokumentet är klar. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart)(Document) | Anropas när uppräkningen av dokumentet har påbörjats. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend)(EditableRangeEnd) | Anropas när ett slut på ett redigerbart område påträffas i dokumentet. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart)(EditableRangeStart) | Anropas när en början av ett redigerbart område påträffas i dokumentet. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend)(FieldEnd) | Anropas när ett fält slutar i dokumentet. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator)(FieldSeparator) | Anropas när en fältavgränsare påträffas i dokumentet. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart)(FieldStart) | Anropas när ett fält startar i dokumentet. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend)(Footnote) | Anropas när uppräkningen av en fotnot eller slutnotstext har avslutats. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart)(Footnote) | Anropas när uppräkningen av en fotnot eller slutnotstext har börjat. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield)(FormField) | Anropas när ett formulärfält påträffas i dokumentet. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend)(GlossaryDocument) | Anropas när uppräkningen av ett ordlistadokument har avslutats. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart)(GlossaryDocument) | Anropas när uppräkning av ett ordlistadokument har påbörjats. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend)(GroupShape) | Anropas när uppräkningen av en gruppform har avslutats. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart)(GroupShape) | Anropas när uppräkningen av en gruppform har börjat. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend)(HeaderFooter) | Anropas när uppräkningen av en sidhuvud eller sidfot i ett avsnitt har avslutats. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart)(HeaderFooter) | Anropas när uppräkningen av en sidhuvud eller sidfot i ett avsnitt har börjat. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend)(OfficeMath) | Anropas när uppräkningen av ett Office Math-objekt har avslutats. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart)(OfficeMath) | Anropas när uppräkningen av ett Office Math-objekt har startat. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend)(Paragraph) | Anropas när uppräkningen av ett stycke har avslutats. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart)(Paragraph) | Anropas när uppräkningen av ett stycke har börjat. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend)(Row) | Anropas när uppräkningen av en tabellrad har avslutats. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart)(Row) | Anropas när uppräkningen av en tabellrad har påbörjats. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun)(Run) | Anropas när en körning av text i den påträffas. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend)(Section) | Anropas när uppräkningen av ett avsnitt har avslutats. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart)(Section) | Anropas när uppräkningen av ett avsnitt har börjat. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend)(Shape) | Anropas när uppräkningen av en form har avslutats. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart)(Shape) | Anropas när uppräkningen av en form har börjat. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend)(SmartTag) | Anropas när uppräkningen av en smart tagg har avslutats. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart)(SmartTag) | Anropas när uppräkningen av en smart tagg har börjat. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar)(SpecialChar) | Ringde när en[`SpecialChar`](../specialchar) nod påträffas i dokumentet. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend)(StructuredDocumentTag) | Anropas när uppräkningen av en strukturerad dokumenttagg har avslutats. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart)(StructuredDocumentTag) | Anropas när uppräkningen av en strukturerad dokumenttagg har startat. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument)(SubDocument) | Anropas när ett underdokument påträffas. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend)(Table) | Anropas när uppräkningen av en tabell är avslutad. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart)(Table) | Anropas när uppräkningen av en tabell har påbörjats. |

### Anmärkningar

Med **DocumentVisitor** du kan definiera och köra anpassade operationer som kräver uppräkning över dokumentträdet.

Till exempel använder Aspose.Words **DocumentVisitor** internt för att spara **Dokumentera** i olika format och för andra operationer som att hitta fält eller bokmärken över ett fragment av ett dokument.

Att använda **DocumentVisitor**:

1. Skapa en klass som härrör från **DocumentVisitor**.
2. Åsidosätt och tillhandahåll implementeringar för några eller alla VisitXXX-metoderna för att utföra vissa anpassade operationer.
3. Ringa upp[`Node.Acceptera`](../node/accept) på **Nod** that du vill börja uppräkningen från.

**DocumentVisitor**tillhandahåller standardimplementeringar för alla VisitXXX-metoderna för att göra det enklare att skapa nya dokumentbesökare eftersom endast de metoder som krävs för den särskilda -besökaren behöver åsidosättas. Det är inte nödvändigt att åsidosätta alla besöksmetoder.

För mer information se Visitor design mönster.

### Exempel

Visar hur man använder en dokumentbesökare för att skriva ut ett dokuments nodstruktur.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // När vi får en sammansatt nod att acceptera en dokumentbesökare, besöker besökaren den accepterande noden,
    // och sedan korsar alla nodens barn på ett djup-först sätt.
    // Besökaren kan läsa och ändra varje besökt nod.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Går igenom en nods träd med undernoder.
/// Skapar en karta över detta träd i form av en sträng.
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
    /// Anropas när en dokumentnod påträffas.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Tillåt besökaren att fortsätta besöka andra noder.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder i en dokumentnod har besökts.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en sektionsnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Hämta indexet för vår sektion i dokumentet.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder i en sektionsnod har besökts.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en Body-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Kallas efter att alla underordnade noder i en Kroppsnod har besökts.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en Paragraph-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas efter att alla undernoder i en Paragraph-nod har besökts.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en körnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en SubDocument-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Lägg till en rad i StringBuilder och dra in den beroende på hur djupt besökaren befinner sig i dokumentträdet.
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

### Se även

* namnutrymme [Aspose.Words](../../aspose.words)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
