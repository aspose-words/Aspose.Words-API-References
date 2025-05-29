---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words für .NET
description: Erstellen und passen Sie Ihre Run-Klasseninstanz mühelos an. Schalten Sie leistungsstarke Funktionen für optimierte Leistung und erweiterte Funktionalität frei.
type: docs
weight: 10
url: /de/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Initialisiert eine neue Instanz des[`Run`](../) Klasse.

```csharp
public Run(DocumentBase doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |

## Bemerkungen

Wann[`Run`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../node/parentnode/) Ist`null`.

Anhängen[`Run`](../) zur Dokumentenverwendung[`InsertAfter`](../../compositenode/insertafter/) oder[`InsertBefore`](../../compositenode/insertbefore/) auf dem Absatz, in den Sie den Lauf einfügen möchten.

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

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

Initialisiert eine neue Instanz des**Laufen** Klasse.

```csharp
public Run(DocumentBase doc, string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| text | String | Der Text des Laufs. |

## Bemerkungen

Wann[`Run`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../node/parentnode/) Ist`null`.

Anhängen[`Run`](../) zur Dokumentenverwendung[`InsertAfter`](../../compositenode/insertafter/) oder[`InsertBefore`](../../compositenode/insertbefore/) auf dem Absatz, in den Sie den Lauf einfügen möchten.

## Beispiele

Zeigt, wie ein Textlauf mithilfe seiner Schriftarteigenschaft formatiert wird.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Siehe auch

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
