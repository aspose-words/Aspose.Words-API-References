---
title: DocumentVisitor.VisitHeaderFooterEnd
linktitle: VisitHeaderFooterEnd
articleTitle: VisitHeaderFooterEnd
second_title: Aspose.Words für .NET
description: DocumentVisitor VisitHeaderFooterEnd methode. Wird aufgerufen wenn die Aufzählung einer Kopf oder Fußzeile in einem Abschnitt beendet wurde in C#.
type: docs
weight: 280
url: /de/net/aspose.words/documentvisitor/visitheaderfooterend/
---
## DocumentVisitor.VisitHeaderFooterEnd method

Wird aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt beendet wurde.

```csharp
public virtual VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooter | HeaderFooter | Das Objekt, das besucht wird. |

### Rückgabewert

A[`VisitorAction`](../../visitoraction/) Wert, der angibt, wie die Enumeration fortgesetzt werden soll.

## Beispiele

Zeigt, wie die Knotenstruktur jeder Kopf- und Fußzeile in einem Dokument gedruckt wird.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Wenn wir einen zusammengesetzten Knoten erhalten, der einen Dokumentbesucher akzeptiert, besucht der Besucher den akzeptierenden Knoten.
    // und durchläuft dann alle untergeordneten Knoten des Knotens in einer Tiefe-zuerst-Methode.
    // Der Besucher kann jeden besuchten Knoten lesen und ändern.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Eine alternative Möglichkeit, abschnittsweise auf die Kopf-/Fußzeilen eines Dokuments zuzugreifen, ist der Zugriff auf die Sammlung.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Durchläuft den nicht-binären Baum der untergeordneten Knoten eines Knotens.
/// Erstellt eine Karte in Form einer Zeichenfolge aller gefundenen HeaderFooter-Knoten und ihrer untergeordneten Knoten.
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
    /// Hängen Sie eine Zeile an den StringBuilder an und rücken Sie sie ein, je nachdem, wie tief sich der Besucher im Dokumentbaum befindet.
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
* class [HeaderFooter](../../headerfooter/)
* class [DocumentVisitor](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
