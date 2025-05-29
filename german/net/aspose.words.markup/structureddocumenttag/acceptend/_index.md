---
title: StructuredDocumentTag.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: Aspose.Words für .NET
description: Entdecken Sie die AcceptEnd-Methode von StructuredDocumentTag – verwalten Sie Besucherinteraktionen am Ende Ihrer strukturierten Dokumente effizient für eine nahtlose Verarbeitung.
type: docs
weight: 340
url: /de/net/aspose.words.markup/structureddocumenttag/acceptend/
---
## StructuredDocumentTag.AcceptEnd method

Akzeptiert einen Besucher für den Besuch des Endes des StructuredDocumentTag.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Dokumentbesucher. |

### Rückgabewert

Die vom Besucher auszuführende Aktion.

## Beispiele

Zeigt, wie die Knotenstruktur jedes strukturierten Dokument-Tags in einem Dokument gedruckt wird.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // Wenn wir einen zusammengesetzten Knoten dazu bringen, einen Dokumentbesucher zu akzeptieren, besucht der Besucher den akzeptierenden Knoten.
    // und durchläuft dann alle untergeordneten Knoten in einer Tiefensuche.
    // Der Besucher kann jeden besuchten Knoten lesen und ändern.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Durchläuft den nicht-binären Baum der untergeordneten Knoten eines Knotens.
/// Erstellt eine Zuordnung in Form einer Zeichenfolge aller gefundenen StructuredDocumentTag-Knoten und ihrer untergeordneten Elemente.
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
    }

    /// <summary>
    /// Ruft den Klartext des vom Besucher gesammelten Dokuments ab.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein StructuredDocumentTag-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines StructuredDocumentTag-Knotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Fügen Sie dem StringBuilder eine Zeile hinzu und rücken Sie sie ein, je nachdem, wie tief der Besucher im Dokumentbaum ist.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private readonly bool mVisitorIsInsideStructuredDocumentTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Siehe auch

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
