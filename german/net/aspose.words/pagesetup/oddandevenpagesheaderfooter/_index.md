---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup OddAndEvenPagesHeaderFooter-Eigenschaft für eindeutige Kopf- und Fußzeilen auf ungeraden und geraden Seiten und verbessern Sie so die Präsentation Ihres Dokuments.
type: docs
weight: 280
url: /de/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

Wahr, wenn das Dokument unterschiedliche Kopf- und Fußzeilen für Seiten mit ungeraden und geraden Seitennummern hat.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Bemerkungen

Beachten Sie, dass sich das Ändern dieser Eigenschaft auf alle Abschnitte im Dokument auswirkt.

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

Zeigt, wie man sogar Seitenkopf-/-fußzeilen aktiviert oder deaktiviert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Arten von Kopf-/Fußzeilen.
// 1 – Die „primäre“ Kopf-/Fußzeile, die auf jeder Seite im Abschnitt angezeigt wird.
// Wir können die primäre Kopf-/Fußzeile durch eine erste und eine gerade Seitenkopf-/Fußzeile überschreiben.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 – Die Kopf-/Fußzeile „Gerade“, die auf jeder geraden Seite dieses Abschnitts erscheint.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Jeder Abschnitt verfügt über ein „PageSetup“-Objekt, das die Eigenschaften für das Erscheinungsbild der Seite angibt
// wie Ausrichtung, Größe und Ränder.
// Setzen Sie die Eigenschaft „OddAndEvenPagesHeaderFooter“ auf „true“
// um die Kopf-/Fußzeile der geraden Seite auf geraden Seiten anzuzeigen.
// Setzen Sie die Eigenschaft „OddAndEvenPagesHeaderFooter“ auf „false“
// um die primäre Kopf-/Fußzeile auf geraden Seiten anzuzeigen.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
