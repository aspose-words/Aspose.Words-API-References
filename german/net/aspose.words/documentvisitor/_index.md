---
title: DocumentVisitor Class
linktitle: DocumentVisitor
articleTitle: DocumentVisitor
second_title: Aspose.Words für .NET
description: Aspose.Words.DocumentVisitor klas. Basisklasse für benutzerdefinierte Dokumentbesucher in C#.
type: docs
weight: 470
url: /de/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Basisklasse für benutzerdefinierte Dokumentbesucher.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public abstract class DocumentVisitor
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(*[AbsolutePositionTab](../absolutepositiontab/)*) | Wird aufgerufen, wenn a[`AbsolutePositionTab`](../absolutepositiontab/) Knoten wird im Dokument gefunden. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(*[Body](../body/)*) | Wird aufgerufen, wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt beendet ist. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(*[Body](../body/)*) | Wird aufgerufen, wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt begonnen hat. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(*[BookmarkEnd](../bookmarkend/)*) | Wird aufgerufen, wenn im Dokument das Ende eines Lesezeichens festgestellt wird. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(*[BookmarkStart](../bookmarkstart/)*) | Wird aufgerufen, wenn im Dokument der Anfang eines Lesezeichens gefunden wird. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | Wird aufgerufen, wenn die Aufzählung eines Bausteins beendet wurde. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | Wird aufgerufen, wenn die Aufzählung eines Bausteins begonnen hat. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(*[Cell](../../aspose.words.tables/cell/)*) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle beendet wurde. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(*[Cell](../../aspose.words.tables/cell/)*) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle gestartet wurde. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(*[Comment](../comment/)*) | Wird aufgerufen, wenn die Aufzählung eines Kommentartextes beendet wurde. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(*[CommentRangeEnd](../commentrangeend/)*) | Wird aufgerufen, wenn das Ende eines kommentierten Textbereichs erreicht wird. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(*[CommentRangeStart](../commentrangestart/)*) | Wird aufgerufen, wenn der Anfang eines kommentierten Textbereichs gefunden wird. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(*[Comment](../comment/)*) | Wird aufgerufen, wenn die Aufzählung eines Kommentartextes gestartet wurde. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(*[Document](../document/)*) | Wird aufgerufen, wenn die Aufzählung des Dokuments abgeschlossen ist. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(*[Document](../document/)*) | Wird aufgerufen, wenn die Aufzählung des Dokuments begonnen hat. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(*[EditableRangeEnd](../editablerangeend/)*) | Wird aufgerufen, wenn im Dokument das Ende eines bearbeitbaren Bereichs erreicht wird. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(*[EditableRangeStart](../editablerangestart/)*) | Wird aufgerufen, wenn im Dokument der Anfang eines bearbeitbaren Bereichs gefunden wird. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(*[FieldEnd](../../aspose.words.fields/fieldend/)*) | Wird aufgerufen, wenn ein Feld im Dokument endet. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(*[FieldSeparator](../../aspose.words.fields/fieldseparator/)*) | Wird aufgerufen, wenn im Dokument ein Feldtrennzeichen gefunden wird. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(*[FieldStart](../../aspose.words.fields/fieldstart/)*) | Wird aufgerufen, wenn ein Feld im Dokument beginnt. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(*[Footnote](../../aspose.words.notes/footnote/)*) | Wird aufgerufen, wenn die Aufzählung eines Fußnoten- oder Endnotentextes beendet wurde. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(*[Footnote](../../aspose.words.notes/footnote/)*) | Wird aufgerufen, wenn die Aufzählung eines Fußnoten- oder Endnotentextes begonnen hat. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(*[FormField](../../aspose.words.fields/formfield/)*) | Wird aufgerufen, wenn im Dokument ein Formularfeld gefunden wird. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | Wird aufgerufen, wenn die Aufzählung eines Glossardokuments beendet wurde. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | Wird aufgerufen, wenn die Aufzählung eines Glossardokuments begonnen hat. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | Wird aufgerufen, wenn die Aufzählung einer Gruppenform beendet wurde. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | Wird aufgerufen, wenn die Aufzählung einer Gruppenform begonnen hat. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(*[HeaderFooter](../headerfooter/)*) | Wird aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt beendet wurde. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(*[HeaderFooter](../headerfooter/)*) | Wird aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt begonnen hat. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Wird aufgerufen, wenn die Aufzählung eines Office Math-Objekts beendet wurde. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Wird aufgerufen, wenn die Aufzählung eines Office Math-Objekts gestartet wurde. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(*[Paragraph](../paragraph/)*) | Wird aufgerufen, wenn die Aufzählung eines Absatzes beendet wurde. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(*[Paragraph](../paragraph/)*) | Wird aufgerufen, wenn die Aufzählung eines Absatzes begonnen hat. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(*[Row](../../aspose.words.tables/row/)*) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzeile beendet wurde. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(*[Row](../../aspose.words.tables/row/)*) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzeile gestartet wurde. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(*[Run](../run/)*) | Wird aufgerufen, wenn eine Textzeile im gefunden wird. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(*[Section](../section/)*) | Wird aufgerufen, wenn die Aufzählung eines Abschnitts beendet wurde. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(*[Section](../section/)*) | Wird aufgerufen, wenn die Aufzählung eines Abschnitts begonnen hat. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(*[Shape](../../aspose.words.drawing/shape/)*) | Wird aufgerufen, wenn die Aufzählung einer Form beendet wurde. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(*[Shape](../../aspose.words.drawing/shape/)*) | Wird aufgerufen, wenn die Aufzählung einer Form begonnen hat. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | Wird aufgerufen, wenn die Aufzählung eines Smarttags beendet wurde. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | Wird aufgerufen, wenn die Aufzählung eines Smarttags gestartet wurde. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(*[SpecialChar](../specialchar/)*) | Wird aufgerufen, wenn a[`SpecialChar`](../specialchar/) Knoten wird im Dokument gefunden. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | Wird aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags beendet wurde. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(*[StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/)*) | Wird aufgerufen, wenn ein StructuredDocumentTagRangeEnd gefunden wird. |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(*[StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/)*) | Wird aufgerufen, wenn ein StructuredDocumentTagRangeStart gefunden wird. |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | Wird aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags begonnen hat. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(*[SubDocument](../subdocument/)*) | Wird aufgerufen, wenn ein Unterdokument gefunden wird. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(*[Table](../../aspose.words.tables/table/)*) | Wird aufgerufen, wenn die Aufzählung einer Tabelle beendet wurde. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(*[Table](../../aspose.words.tables/table/)*) | Wird aufgerufen, wenn die Aufzählung einer Tabelle gestartet wurde. |

## Bemerkungen

Mit`DocumentVisitor` Sie können benutzerdefinierte Vorgänge definieren und ausführen, die eine Aufzählung über den Dokumentbaum erfordern.

Aspose.Words verwendet beispielsweise`DocumentVisitor` intern zum Speichern[`Document`](../document/) in verschiedenen Formaten und für andere Vorgänge wie das Suchen von Feldern oder Lesezeichen über ein Fragment eines Dokuments.

Benutzen`DocumentVisitor`:

1. Erstellen Sie eine von abgeleitete Klasse`DocumentVisitor`.
2. Überschreiben und stellen Sie Implementierungen für einige oder alle VisitXXX-Methoden bereit, um einige benutzerdefinierte Vorgänge auszuführen.
3. Anruf[`Node.Accept`](../node/accept/) auf der[`Node`](../node/) that , von dem aus Sie die Aufzählung starten möchten.

`DocumentVisitor` stellt Standardimplementierungen für alle VisitXXX-Methoden bereit, um das Erstellen neuer Dokumentbesucher zu vereinfachen, da nur die Methoden überschrieben werden müssen, die für den bestimmten -Besucher erforderlich sind. Es ist nicht notwendig, alle Besuchermethoden zu überschreiben.

Weitere Informationen finden Sie im Besucherentwurfsmuster.

## Beispiele

Zeigt, wie ein Dokumentbesucher zum Drucken der Knotenstruktur eines Dokuments verwendet wird.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Wenn wir einen zusammengesetzten Knoten erhalten, der einen Dokumentbesucher akzeptiert, besucht der Besucher den akzeptierenden Knoten.
    // und durchläuft dann alle untergeordneten Knoten des Knotens in einer Tiefe-zuerst-Methode.
    // Der Besucher kann jeden besuchten Knoten lesen und ändern.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Durchläuft den Baum der untergeordneten Knoten eines Knotens.
/// Erstellt eine Karte dieses Baums in Form einer Zeichenfolge.
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
    /// Wird aufgerufen, wenn ein Document-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Dem Besucher erlauben, weiterhin andere Knoten zu besuchen.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Dokumentknotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Abschnittsknoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Holen Sie sich den Index unseres Abschnitts innerhalb des Dokuments.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Abschnittsknotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Body-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Body-Knotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Paragraph-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Absatzknotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein SubDocument-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Hängen Sie eine Zeile an den StringBuilder an und rücken Sie sie ein, je nachdem, wie tief sich der Besucher im Dokumentbaum befindet.
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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
