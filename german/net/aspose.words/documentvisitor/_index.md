---
title: DocumentVisitor
second_title: Aspose.Words für .NET-API-Referenz
description: Basisklasse für benutzerdefinierte Dokumentbesucher.
type: docs
weight: 460
url: /de/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Basisklasse für benutzerdefinierte Dokumentbesucher.

```csharp
public abstract class DocumentVisitor
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab)(AbsolutePositionTab) | Angerufen, wenn a[`AbsolutePositionTab`](../absolutepositiontab) Knoten wird im Dokument gefunden. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend)(Body) | Wird aufgerufen, wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt beendet ist. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart)(Body) | Wird aufgerufen, wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt begonnen hat. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend)(BookmarkEnd) | Wird aufgerufen, wenn das Ende eines Lesezeichens im Dokument gefunden wird. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart)(BookmarkStart) | Wird aufgerufen, wenn im Dokument der Anfang eines Lesezeichens gefunden wird. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend)(BuildingBlock) | Wird aufgerufen, wenn die Aufzählung eines Bausteins beendet ist. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart)(BuildingBlock) | Wird aufgerufen, wenn die Enumeration eines Bausteins gestartet wurde. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend)(Cell) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle beendet ist. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart)(Cell) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle begonnen hat. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend)(Comment) | Wird aufgerufen, wenn die Aufzählung eines Kommentartextes beendet ist. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend)(CommentRangeEnd) | Wird aufgerufen, wenn das Ende eines kommentierten Textbereichs erreicht wird. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart)(CommentRangeStart) | Wird aufgerufen, wenn der Anfang eines kommentierten Textbereichs gefunden wird. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart)(Comment) | Wird aufgerufen, wenn die Aufzählung eines Kommentartextes begonnen hat. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend)(Document) | Wird aufgerufen, wenn die Aufzählung des Dokuments abgeschlossen ist. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart)(Document) | Wird aufgerufen, wenn die Aufzählung des Dokuments gestartet wurde. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend)(EditableRangeEnd) | Wird aufgerufen, wenn im Dokument ein Ende eines bearbeitbaren Bereichs gefunden wird. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart)(EditableRangeStart) | Wird aufgerufen, wenn im Dokument ein Anfang eines bearbeitbaren Bereichs gefunden wird. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend)(FieldEnd) | Wird aufgerufen, wenn ein Feld im Dokument endet. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator)(FieldSeparator) | Wird aufgerufen, wenn im Dokument ein Feldtrennzeichen gefunden wird. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart)(FieldStart) | Wird aufgerufen, wenn ein Feld im Dokument beginnt. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend)(Footnote) | Wird aufgerufen, wenn die Aufzählung eines Fußnoten- oder Endnotentexts beendet ist. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart)(Footnote) | Wird aufgerufen, wenn die Aufzählung eines Fußnoten- oder Endnotentextes begonnen hat. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield)(FormField) | Wird aufgerufen, wenn ein Formularfeld im Dokument gefunden wird. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend)(GlossaryDocument) | Wird aufgerufen, wenn die Aufzählung eines Glossardokuments beendet ist. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart)(GlossaryDocument) | Wird aufgerufen, wenn die Aufzählung eines Glossardokuments begonnen hat. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend)(GroupShape) | Wird aufgerufen, wenn die Aufzählung einer Gruppenform beendet ist. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart)(GroupShape) | Wird aufgerufen, wenn die Aufzählung einer Gruppenform begonnen hat. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend)(HeaderFooter) | Wird aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt beendet ist. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart)(HeaderFooter) | Wird aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt begonnen hat. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend)(OfficeMath) | Wird aufgerufen, wenn die Aufzählung eines Office Math-Objekts beendet ist. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart)(OfficeMath) | Wird aufgerufen, wenn die Aufzählung eines Office Math-Objekts gestartet wurde. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend)(Paragraph) | Wird aufgerufen, wenn die Aufzählung eines Absatzes beendet ist. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart)(Paragraph) | Wird aufgerufen, wenn die Aufzählung eines Absatzes begonnen hat. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend)(Row) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzeile beendet ist. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart)(Row) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzeile begonnen hat. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun)(Run) | Wird aufgerufen, wenn eine Textfolge im gefunden wird. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend)(Section) | Wird aufgerufen, wenn die Aufzählung eines Abschnitts beendet ist. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart)(Section) | Wird aufgerufen, wenn die Aufzählung eines Abschnitts begonnen hat. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend)(Shape) | Wird aufgerufen, wenn die Aufzählung einer Form beendet ist. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart)(Shape) | Wird aufgerufen, wenn die Aufzählung einer Form begonnen hat. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend)(SmartTag) | Wird aufgerufen, wenn die Aufzählung eines Smarttags beendet ist. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart)(SmartTag) | Wird aufgerufen, wenn die Aufzählung eines Smarttags begonnen hat. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar)(SpecialChar) | Angerufen, wenn a[`SpecialChar`](../specialchar) Knoten wird im Dokument gefunden. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend)(StructuredDocumentTag) | Wird aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags beendet ist. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart)(StructuredDocumentTag) | Wird aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags begonnen hat. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument)(SubDocument) | Wird aufgerufen, wenn ein Unterdokument gefunden wird. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend)(Table) | Wird aufgerufen, wenn die Aufzählung einer Tabelle beendet ist. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart)(Table) | Wird aufgerufen, wenn die Aufzählung einer Tabelle gestartet wurde. |

### Bemerkungen

Mit **DokumentBesucher** Sie können benutzerdefinierte Operationen definieren und ausführen, die eine Aufzählung über den Dokumentbaum erfordern.

Beispielsweise verwendet Aspose.Words **DokumentBesucher** intern zum Speichern **Dokumentieren** in verschiedenen Formaten und für andere Operationen wie das Suchen von Feldern oder Lesezeichen über einem Fragment eines Dokuments.

Benutzen **DokumentBesucher**:

1. Erstellen Sie eine abgeleitete Klasse **DokumentBesucher**.
2. Überschreiben und stellen Sie Implementierungen für einige oder alle VisitXXX-Methoden bereit, um einige benutzerdefinierte Operationen auszuführen.
3. Anruf[`Knoten.Akzeptieren`](../node/accept) auf der **Knoten** that , von dem aus Sie die Aufzählung starten möchten.

**DokumentBesucher**bietet Standardimplementierungen für alle VisitXXX-Methoden , um das Erstellen neuer Dokumentbesucher zu vereinfachen, da nur die Methoden überschrieben werden müssen, die für den jeweiligen -Besucher erforderlich sind. Es ist nicht erforderlich, alle Besuchermethoden zu überschreiben.

Weitere Informationen finden Sie im Besucher-Entwurfsmuster.

### Beispiele

Zeigt, wie ein Dokument-Besucher verwendet wird, um die Knotenstruktur eines Dokuments zu drucken.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Wenn wir einen zusammengesetzten Knoten dazu bringen, einen Dokumentbesucher zu akzeptieren, besucht der Besucher den akzeptierenden Knoten,
    // und durchläuft dann alle untergeordneten Elemente des Knotens mit der Tiefe zuerst.
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
    /// Wird aufgerufen, wenn ein Dokumentknoten gefunden wird.
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
    /// Eine Zeile an den StringBuilder anhängen und einrücken, je nachdem, wie tief der Besucher in den Dokumentenbaum eindringt.
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

* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
