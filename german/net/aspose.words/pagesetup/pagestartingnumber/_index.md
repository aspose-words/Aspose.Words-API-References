---
title: PageSetup.PageStartingNumber
linktitle: PageStartingNumber
articleTitle: PageStartingNumber
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup-Eigenschaft PageStartingNumber, um die Startseitenzahl Ihres Dokuments einfach anzupassen und so für mehr Ordnung und Übersichtlichkeit zu sorgen.
type: docs
weight: 330
url: /de/net/aspose.words/pagesetup/pagestartingnumber/
---
## PageSetup.PageStartingNumber property

Ruft die Startseitennummer des Abschnitts ab oder legt sie fest.

```csharp
public int PageStartingNumber { get; set; }
```

## Bemerkungen

Die[`RestartPageNumbering`](../restartpagenumbering/) Eigenschaft, wenn gesetzt auf`FALSCH` , überschreibt the `PageStartingNumber` Eigenschaft, damit die Seitennummerierung vom vorherigen Abschnitt fortgesetzt werden kann.

## Beispiele

Zeigt, wie die Seitennummerierung in einem Abschnitt eingerichtet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Verschieben Sie den Dokumentgenerator in die primäre Kopfzeile des ersten Abschnitts.
// die auf jeder Seite in diesem Abschnitt angezeigt wird.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Fügen Sie ein PAGE-Feld ein, das die Nummer der aktuellen Seite anzeigt.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Konfigurieren Sie den Abschnitt so, dass die in den PAGE-Feldern angezeigte Seitenanzahl bei 5 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass ihre Seitenzahlen mit römischen Großbuchstaben angezeigt werden.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Erstellen Sie eine weitere primäre Kopfzeile für den zweiten Abschnitt mit einem weiteren PAGE-Feld.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Konfigurieren Sie den Abschnitt so, dass die in den PAGE-Feldern angezeigte Seitenanzahl bei 10 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass ihre Seitenzahlen mit arabischen Zahlen angezeigt werden.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
