---
title: Node.GetText
second_title: Aspose.Words für .NET-API-Referenz
description: Node methode. Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab.
type: docs
weight: 120
url: /de/net/aspose.words/node/gettext/
---
## Node.GetText method

Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab.

```csharp
public virtual string GetText()
```

### Bemerkungen

Die zurückgegebene Zeichenfolge enthält alle Steuer- und Sonderzeichen, wie in beschrieben[`ControlChar`](../../controlchar/).

### Beispiele

Zeigt, wie Steuerzeichen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Mit DocumentBuilder Absätze mit Text einfügen.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Beim Konvertieren des Dokuments in Textform werden die Steuerzeichen sichtbar
// stellen einige der Strukturelemente des Dokuments dar, z. B. Seitenumbrüche.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Beim Konvertieren eines Dokuments in String-Form,
// Mit der Trim-Methode können wir einige Steuerzeichen weglassen.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

Zeigt, wie man ein Aspose.Words-Dokument manuell erstellt.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält einen Abschnitt, einen Hauptteil und einen Absatz.
// Rufen Sie die Methode „RemoveAllChildren“ auf, um alle diese Knoten zu entfernen.
// und erhalten am Ende einen Dokumentknoten ohne untergeordnete Elemente.
doc.RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten untergeordneten Knoten, denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu füllen.
// Erstellen Sie zunächst einen neuen Abschnitt und hängen Sie ihn dann als untergeordnetes Element an den Stammdokumentknoten an.
Section section = new Section(doc);
doc.AppendChild(section);

// Legen Sie einige Seiteneinrichtungseigenschaften für den Abschnitt fest.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Ein Abschnitt benötigt einen Hauptteil, der seinen gesamten Inhalt enthält und anzeigt
// auf der Seite zwischen Kopf- und Fußzeile des Abschnitts.
Body body = new Body(doc);
section.AppendChild(body);

// Einen Absatz erstellen, einige Formatierungseigenschaften festlegen und ihn dann als untergeordnetes Element an den Text anhängen.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Zum Schluss fügen Sie etwas Inhalt hinzu, um das Dokument zu erstellen. Erstellen Sie einen Lauf,
// Aussehen und Inhalt festlegen und dann als untergeordnetes Element an den Absatz anhängen.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Siehe auch

* class [Node](../)
* namensraum [Aspose.Words](../../node/)
* Montage [Aspose.Words](../../../)


