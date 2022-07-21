---
title: VisitBodyEnd
second_title: Aspose.Words für .NET-API-Referenz
description: Wird aufgerufen wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt beendet ist.
type: docs
weight: 20
url: /de/net/aspose.words/documentvisitor/visitbodyend/
---
## DocumentVisitor.VisitBodyEnd method

Wird aufgerufen, wenn die Aufzählung der Haupttextgeschichte in einem Abschnitt beendet ist.

```csharp
public virtual VisitorAction VisitBodyEnd(Body body)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| body | Body | Das Objekt, das besucht wird. |

### Rückgabewert

EIN[`VisitorAction`](../../visitoraction) Wert, der angibt, wie die Enumeration fortgesetzt werden soll.

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

* enum [VisitorAction](../../visitoraction)
* class [Body](../../body)
* class [DocumentVisitor](../../documentvisitor)
* namensraum [Aspose.Words](../../documentvisitor)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
