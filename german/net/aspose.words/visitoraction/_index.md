---
title: VisitorAction Enum
linktitle: VisitorAction
articleTitle: VisitorAction
second_title: Aspose.Words für .NET
description: Erkunden Sie Aspose.Words.VisitorAction-Enumeration, um die Knotenaufzählung mühelos zu verwalten und so die Effizienz und Kontrolle Ihrer Dokumentverarbeitung zu verbessern.
type: docs
weight: 7470
url: /de/net/aspose.words/visitoraction/
---
## VisitorAction enumeration

Ermöglicht dem Besucher, die Aufzählung der Knoten zu steuern.

```csharp
public enum VisitorAction
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Continue | `0` | Der Besucher fordert die Fortsetzung der Aufzählung an. |
| SkipThisNode | `1` | Der Besucher fordert an, den aktuellen Knoten zu überspringen und mit der Aufzählung fortzufahren. |
| Stop | `2` | Der Besucher fordert die Beendigung der Knotenaufzählung an. |

## Beispiele

Zeigt, wie Tabulatorzeichen mit absoluter Position mit einem Dokumentbesucher verarbeitet werden.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extrahieren Sie den Textinhalt unseres Dokuments, indem Sie diesen benutzerdefinierten Dokumentbesucher akzeptieren.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Besuchen Sie nur den Anfang des Dokumenttexts.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Besuchen Sie nur das Ende des Dokumenttexts.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // Die absolute Position Tab, für die es kein Äquivalent in Stringform gibt, wurde explizit in ein Tabulatorzeichen umgewandelt.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Ein AbsolutePositionTab kann auch selbst einen DocumentVisitor akzeptieren.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Sammelt den Textinhalt aller Läufe im besuchten Dokument. Ersetzt alle absoluten Tabulatorzeichen durch normale Tabulatoren.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein AbsolutePositionTab-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Fügt der aktuellen Ausgabe Text hinzu. Beachtet das aktivierte/deaktivierte Ausgabeflag.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Klartext des vom Besucher gesammelten Dokuments.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
