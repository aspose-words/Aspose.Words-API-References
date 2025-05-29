---
title: Footnote.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words für .NET
description: Entdecken Sie die Footnote-Accept-Methode, um die Besucherinteraktion zu verbessern und das Benutzererlebnis Ihrer Website zu optimieren. Steigern Sie noch heute Ihre Conversions!
type: docs
weight: 80
url: /de/net/aspose.words.notes/footnote/accept/
---
## Footnote.Accept method

Nimmt einen Besucher auf.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Besucher, der die Knoten besuchen wird. |

### Rückgabewert

Wahr, wenn alle Knoten besucht wurden; falsch, wenn[`DocumentVisitor`](../../../aspose.words/documentvisitor/) hat den Vorgang abgebrochen, bevor alle Knoten besucht wurden.

## Bemerkungen

Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft eine entsprechende Methode auf[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Besucher-Entwurfsmuster.

Ruft DocumentVisitor.VisitFootnoteStart auf, ruft dann Accept für alle untergeordneten Knoten der Fußnote auf und ruft am Ende DocumentVisitor.VisitFootnoteEnd auf.

## Beispiele

Zeigt, wie die Knotenstruktur jeder Fußnote in einem Dokument gedruckt wird.

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // Wenn wir einen zusammengesetzten Knoten dazu bringen, einen Dokumentbesucher zu akzeptieren, besucht der Besucher den akzeptierenden Knoten.
    // und durchläuft dann alle untergeordneten Knoten in einer Tiefensuche.
    // Der Besucher kann jeden besuchten Knoten lesen und ändern.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Durchläuft den nicht-binären Baum der untergeordneten Knoten eines Knotens.
/// Erstellt eine Karte in Form einer Zeichenfolge aller gefundenen Fußnotenknoten und ihrer untergeordneten Elemente.
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// Ruft den Klartext des vom Besucher gesammelten Dokuments ab.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Fußnotenknoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Fußnotenknotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

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

    private bool mVisitorIsInsideFootnote;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Siehe auch

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
