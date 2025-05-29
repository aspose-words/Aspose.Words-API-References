---
title: Run.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihren Fließtext mühelos! Rufen Sie Fließtexteigenschaften einfach ab oder legen Sie sie fest, um eine nahtlose Dokumentbearbeitung und verbesserte Inhaltskontrolle zu gewährleisten.
type: docs
weight: 50
url: /de/net/aspose.words/run/text/
---
## Run.Text property

Ruft den Text des Laufs ab oder legt ihn fest.

```csharp
public string Text { get; set; }
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

### Siehe auch

* class [Run](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
