---
title: HeaderFooter.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die HeaderFooter AcceptStart-Methode, die Besucher nahtlos am Anfang der Kopfzeile begrüßt und so das Benutzererlebnis und die Interaktion verbessert.
type: docs
weight: 90
url: /de/net/aspose.words/headerfooter/acceptstart/
---
## HeaderFooter.AcceptStart method

Akzeptiert einen Besucher für den Besuch des Anfangs der Kopfzeile.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Dokumentbesucher. |

### Rückgabewert

Die vom Besucher auszuführende Aktion.

## Beispiele

Zeigt, wie die Knotenstruktur jeder Kopf- und Fußzeile in einem Dokument gedruckt wird.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Wenn wir einen zusammengesetzten Knoten dazu bringen, einen Dokumentbesucher zu akzeptieren, besucht der Besucher den akzeptierenden Knoten.
    // und durchläuft dann alle untergeordneten Knoten in einer Tiefensuche.
    // Der Besucher kann jeden besuchten Knoten lesen und ändern.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Eine alternative Möglichkeit, abschnittsweise auf die Kopf-/Fußzeilen eines Dokuments zuzugreifen, ist der Zugriff auf die Sammlung.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Durchläuft den nicht-binären Baum der untergeordneten Knoten eines Knotens.
/// Erstellt eine Karte in Form einer Zeichenfolge aller gefundenen HeaderFooter-Knoten und ihrer untergeordneten Elemente.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein HeaderFooter-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines HeaderFooter-Knotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

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

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Siehe auch

* enum [VisitorAction](../../visitoraction/)
* class [DocumentVisitor](../../documentvisitor/)
* class [HeaderFooter](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
