---
title: PageSetup.SectionStart
linktitle: SectionStart
articleTitle: SectionStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup SectionStart-Eigenschaft, um Abschnittsumbrüche in Ihrem Dokument einfach zu verwalten. Verbessern Sie noch heute die Formatierung und Layoutkontrolle!
type: docs
weight: 390
url: /de/net/aspose.words/pagesetup/sectionstart/
---
## PageSetup.SectionStart property

Gibt den Typ des Abschnittsumbruchs für das angegebene Objekt zurück oder legt ihn fest.

```csharp
public SectionStart SectionStart { get; set; }
```

## Beispiele

Zeigt, wie man ein Aspose.Words-Dokument manuell erstellt.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält einen Abschnitt, einen Hauptteil und einen Absatz.
// Rufen Sie die Methode „RemoveAllChildren“ auf, um alle diese Knoten zu entfernen.
// und am Ende einen Dokumentknoten ohne untergeordnete Elemente erhalten.
doc.RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten untergeordneten Knoten, denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu füllen.
// Erstellen Sie zuerst einen neuen Abschnitt und hängen Sie ihn dann als untergeordnetes Element an den Stammdokumentknoten an.
Section section = new Section(doc);
doc.AppendChild(section);

// Legen Sie einige Seiteneinrichtungseigenschaften für den Abschnitt fest.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Ein Abschnitt benötigt einen Hauptteil, der seinen gesamten Inhalt enthält und anzeigt
// auf der Seite zwischen Kopf- und Fußzeile des Abschnitts.
Body body = new Body(doc);
section.AppendChild(body);

// Erstellen Sie einen Absatz, legen Sie einige Formatierungseigenschaften fest und hängen Sie ihn dann als untergeordnetes Element an den Textkörper an.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Abschließend fügen Sie dem Dokument noch Inhalt hinzu. Erstellen Sie einen Lauf,
// Legen Sie das Erscheinungsbild und den Inhalt fest und hängen Sie es dann als untergeordnetes Element an den Absatz an.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Zeigt, wie Sie angeben, wie sich ein neuer Abschnitt vom vorherigen abgrenzt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Abschnittsumbruchtypen bestimmen, wie sich ein neuer Abschnitt vom vorherigen Abschnitt abgrenzt.
// Unten sind fünf Arten von Abschnittsumbrüchen aufgeführt.
// 1 – Beginnt den nächsten Abschnitt auf einer neuen Seite:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 – Startet den nächsten Abschnitt auf der aktuellen Seite:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 – Beginnt den nächsten Abschnitt auf einer neuen geraden Seite:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 – Beginnt den nächsten Abschnitt auf einer neuen ungeraden Seite:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 – Beginnt den nächsten Abschnitt in einer neuen Spalte:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Siehe auch

* enum [SectionStart](../../sectionstart/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
