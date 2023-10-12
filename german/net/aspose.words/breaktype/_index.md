---
title: Enum BreakType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.BreakType opsomming. Gibt die Art eines Umbruchs innerhalb eines Dokuments an.
type: docs
weight: 110
url: /de/net/aspose.words/breaktype/
---
## BreakType enumeration

Gibt die Art eines Umbruchs innerhalb eines Dokuments an.

```csharp
public enum BreakType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| ParagraphBreak | `0` | Pause zwischen den Absätzen. |
| PageBreak | `1` | Expliziter Seitenumbruch. |
| ColumnBreak | `2` | Expliziter Spaltenumbruch. |
| SectionBreakContinuous | `3` | Gibt den Beginn eines neuen Abschnitts auf derselben Seite wie der vorherige Abschnitt an. |
| SectionBreakNewColumn | `4` | Gibt den Beginn des neuen Abschnitts in der neuen Spalte an. |
| SectionBreakNewPage | `5` | Gibt den Beginn eines neuen Abschnitts auf einer neuen Seite an. |
| SectionBreakEvenPage | `6` | Gibt den Beginn eines neuen Abschnitts auf einer neuen geraden Seite an. |
| SectionBreakOddPage | `7` | Gibt den Beginn eines neuen Abschnitts auf einer ungeraden Seite an. |
| LineBreak | `8` | Expliziter Zeilenumbruch. |

### Beispiele

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

Zeigt, wie Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument angewendet und wiederhergestellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändern Sie die Seiteneinrichtungseigenschaften für den aktuellen Abschnitt des Builders und fügen Sie Text hinzu.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Wenn wir einen neuen Abschnitt mit einem Document Builder beginnen,
// Es erbt die aktuellen Seiteneinrichtungseigenschaften des Builders.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Mit der Methode „ClearFormatting“ können wir die Seiteneinrichtungseigenschaften auf ihre Standardwerte zurücksetzen.
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

Zeigt, wie man ein Inhaltsverzeichnis (TOC) in ein Dokument einfügt, indem man Überschriftenstile als Einträge verwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Inhaltsverzeichnis für die erste Seite des Dokuments einfügen.
// Konfigurieren Sie die Tabelle so, dass sie Absätze mit Überschriften der Ebenen 1 bis 3 aufnimmt.
// Legen Sie außerdem fest, dass seine Einträge Hyperlinks sind, die uns weiterleiten
// zur Position der Überschrift, wenn in Microsoft Word mit der linken Maustaste darauf geklickt wird.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Füllen Sie das Inhaltsverzeichnis, indem Sie Absätze mit Überschriftenstilen hinzufügen.
// Jede solche Überschrift mit einer Ebene zwischen 1 und 3 erstellt einen Eintrag in der Tabelle.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Ein Inhaltsverzeichnis ist ein Feld eines Typs, der aktualisiert werden muss, um ein aktuelles Ergebnis anzuzeigen.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


