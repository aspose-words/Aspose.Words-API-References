---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words für .NET
description: PageSetup OddAndEvenPagesHeaderFooter eigendom. True wenn das Dokument unterschiedliche Kopf und Fußzeilen für ungeradzahlige und gerade nummerierte Seiten hat in C#.
type: docs
weight: 280
url: /de/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

True, wenn das Dokument unterschiedliche Kopf- und Fußzeilen für ungeradzahlige und gerade nummerierte Seiten hat.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Bemerkungen

Beachten Sie, dass sich die Änderung dieser Eigenschaft auf alle Abschnitte im Dokument auswirkt.

## Beispiele

Zeigt, wie man mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir unterschiedliche Kopf- und Fußzeilen für die erste, gerade und ungerade Seite wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dann drei Seiten zum Dokument hinzu, um jeden Kopfzeilentyp anzuzeigen.
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

Zeigt, wie man gerade Seitenkopf-/Fußzeilen aktiviert oder deaktiviert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend sind zwei Arten von Kopf-/Fußzeilen aufgeführt.
// 1 – Die „primäre“ Kopf-/Fußzeile, die auf jeder Seite im Abschnitt erscheint.
 // Wir können die primäre Kopf-/Fußzeile durch eine erste und eine gerade Seitenkopf-/-fußzeile überschreiben.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 – Die „gerade“ Kopf-/Fußzeile, die auf jeder geraden Seite dieses Abschnitts erscheint.
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

// Jeder Abschnitt verfügt über ein „PageSetup“-Objekt, das Eigenschaften im Zusammenhang mit der Darstellung der Seite angibt
// wie Ausrichtung, Größe und Ränder.
// Setze die Eigenschaft „OddAndEvenPagesHeaderFooter“ auf „true“
// um die Kopf-/Fußzeile der geraden Seite auf geraden Seiten anzuzeigen.
// Setze die Eigenschaft „OddAndEvenPagesHeaderFooter“ auf „false“
// um die primäre Kopf-/Fußzeile auf geraden Seiten anzuzeigen.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
