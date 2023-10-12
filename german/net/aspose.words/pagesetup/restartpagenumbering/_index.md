---
title: PageSetup.RestartPageNumbering
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. True wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt.
type: docs
weight: 360
url: /de/net/aspose.words/pagesetup/restartpagenumbering/
---
## PageSetup.RestartPageNumbering property

True, wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt.

```csharp
public bool RestartPageNumbering { get; set; }
```

### Bemerkungen

Wenn auf eingestellt`FALSCH` , Die`RestartPageNumbering` Die Eigenschaft überschreibt the [`PageStartingNumber`](../pagestartingnumber/) Eigenschaft, damit die Seitennummerierung vom vorherigen Abschnitt fortgesetzt werden kann.

### Beispiele

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

// Den Document Builder in den primären Header des ersten Abschnitts verschieben,
// was auf jeder Seite in diesem Abschnitt angezeigt wird.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Ein PAGE-Feld einfügen, das die Nummer der aktuellen Seite anzeigt.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Konfigurieren Sie den Abschnitt so, dass die Seitenanzahl, die in den PAGE-Feldern angezeigt wird, bei 5 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass ihre Seitenzahlen in großen römischen Ziffern angezeigt werden.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Einen weiteren primären Header für den zweiten Abschnitt mit einem anderen PAGE-Feld erstellen.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Konfigurieren Sie den Abschnitt so, dass die Seitenzahl, die in den PAGE-Feldern angezeigt wird, bei 10 beginnt.
// Konfigurieren Sie außerdem alle PAGE-Felder so, dass ihre Seitenzahlen mit arabischen Zahlen angezeigt werden.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


