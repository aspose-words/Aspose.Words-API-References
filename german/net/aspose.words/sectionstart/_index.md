---
title: Enum SectionStart
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.SectionStart opsomming. Die Art der Unterbrechung am Anfang des Abschnitts.
type: docs
weight: 5470
url: /de/net/aspose.words/sectionstart/
---
## SectionStart enumeration

Die Art der Unterbrechung am Anfang des Abschnitts.

```csharp
public enum SectionStart
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Continuous | `0` | Der neue Abschnitt beginnt auf derselben Seite wie der vorherige Abschnitt. |
| NewColumn | `1` | Der Abschnitt beginnt in einer neuen Spalte. |
| NewPage | `2` | Der Abschnitt beginnt auf einer neuen Seite. |
| EvenPage | `3` | Der Abschnitt beginnt auf einer neuen geraden Seite. |
| OddPage | `4` | Der Abschnitt beginnt auf einer neuen ungeraden Seite. |

### Beispiele

Zeigt, wie ein Aspose.Words-Dokument von Hand erstellt wird.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält einen Abschnitt, einen Hauptteil und einen Absatz.
// Rufen Sie die Methode "RemoveAllChildren" auf, um alle diese Knoten zu entfernen,
// und am Ende einen Dokumentknoten ohne Kinder haben.
doc.RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten untergeordneten Knoten, denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu füllen.
// Erstellen Sie zuerst einen neuen Abschnitt und hängen Sie ihn dann als untergeordnetes Element an den Stammdokumentknoten an.
Section section = new Section(doc);
doc.AppendChild(section);

// Legen Sie einige Seiteneinrichtungseigenschaften für den Abschnitt fest.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Ein Abschnitt benötigt einen Körper, der seinen gesamten Inhalt enthält und anzeigt
// auf der Seite zwischen Kopf- und Fußzeile des Abschnitts.
Body body = new Body(doc);
section.AppendChild(body);

// Erstellen Sie einen Absatz, legen Sie einige Formatierungseigenschaften fest und hängen Sie ihn dann als untergeordnetes Element an den Textkörper an.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Fügen Sie schließlich etwas Inhalt hinzu, um das Dokument zu erstellen. Erstellen Sie einen Lauf,
// Aussehen und Inhalt festlegen und dann als untergeordnetes Element an den Absatz anhängen.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Zeigt, wie angegeben wird, wie sich ein neuer Abschnitt vom vorherigen trennt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Abschnittsumbruchtypen bestimmen, wie sich ein neuer Abschnitt vom vorherigen Abschnitt trennt.
// Nachfolgend sind fünf Arten von Abschnittsumbrüchen aufgeführt.
// 1 - Beginnt den nächsten Abschnitt auf einer neuen Seite:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - Startet den nächsten Abschnitt auf der aktuellen Seite:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Beginnt den nächsten Abschnitt auf einer neuen geraden Seite:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - Beginnt den nächsten Abschnitt auf einer neuen ungeraden Seite:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - Beginnt den nächsten Abschnitt in einer neuen Spalte:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


