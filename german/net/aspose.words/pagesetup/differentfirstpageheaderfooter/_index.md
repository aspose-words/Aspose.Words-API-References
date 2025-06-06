---
title: PageSetup.DifferentFirstPageHeaderFooter
linktitle: DifferentFirstPageHeaderFooter
articleTitle: DifferentFirstPageHeaderFooter
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup DifferentFirstPageHeaderFooter-Eigenschaft, um die erste Seite Ihres Dokuments mit einzigartigen Kopf- und Fußzeilen für eine professionelle Note anzupassen.
type: docs
weight: 110
url: /de/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

Wahr, wenn auf der ersten Seite eine andere Kopf- oder Fußzeile verwendet wird.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

## Beispiele

Zeigt, wie Sie mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir für die erste, die gerade und die ungerade Seite unterschiedliche Kopf- und Fußzeilen wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dem Dokument dann drei Seiten hinzu, um jeden Kopfzeilentyp anzuzeigen.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Zeigt, wie primäre Kopf-/Fußzeilen aktiviert oder deaktiviert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Arten von Kopf-/Fußzeilen.
// 1 – Die „Erste“ Kopf-/Fußzeile, die auf der ersten Seite des Abschnitts angezeigt wird.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 – Die „primäre“ Kopf-/Fußzeile, die auf jeder Seite im Abschnitt angezeigt wird.
// Wir können die primäre Kopf-/Fußzeile durch eine erste und eine gerade Seitenkopf-/Fußzeile überschreiben.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Jeder Abschnitt verfügt über ein „PageSetup“-Objekt, das die Eigenschaften für das Erscheinungsbild der Seite angibt
// wie Ausrichtung, Größe und Ränder.
// Setzen Sie die Eigenschaft „DifferentFirstPageHeaderFooter“ auf „true“, um die erste Kopf-/Fußzeile auf die erste Seite anzuwenden.
// Setzen Sie die Eigenschaft „DifferentFirstPageHeaderFooter“ auf „false“
// um auf der ersten Seite die primäre Kopf-/Fußzeile anzuzeigen.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

Zeigt, wie die Reihenfolge verfolgt wird, in der ein Textersetzungsvorgang Knoten durchläuft.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // Die Verwendung einer anderen Kopf-/Fußzeile für die erste Seite wirkt sich auf die Suchreihenfolge aus.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Zeichnet während einer Suchen-und-Ersetzen-Operation den Inhalt jedes Knotens auf, der Text enthält, den die Operation „findet“.
/// in dem Zustand, in dem es sich vor dem Austausch befindet.
/// Dadurch wird die Reihenfolge angezeigt, in der der Textersetzungsvorgang die Knoten durchläuft.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
