---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words für .NET
description: Run constructeur. Initialisiert eine neue Instanz vonRun Klasse in C#.
type: docs
weight: 10
url: /de/net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Initialisiert eine neue Instanz von[`Run`](../) Klasse.

```csharp
public Run(DocumentBase doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |

## Bemerkungen

Wann[`Run`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../node/parentnode/) Ist`Null`.

Anhängen[`Run`](../) zur Dokumentenverwendung[`InsertAfter`](../../compositenode/insertafter/) oder[`InsertBefore`](../../compositenode/insertbefore/) an dem Absatz, an dem der Lauf eingefügt werden soll.

## Beispiele

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

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

Initialisiert eine neue Instanz von**Laufen** Klasse.

```csharp
public Run(DocumentBase doc, string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| text | String | Der Text des Laufs. |

## Bemerkungen

Wann[`Run`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../node/parentnode/) Ist`Null`.

Anhängen[`Run`](../) zur Dokumentenverwendung[`InsertAfter`](../../compositenode/insertafter/) oder[`InsertBefore`](../../compositenode/insertbefore/) an dem Absatz, an dem der Lauf eingefügt werden soll.

## Beispiele

Zeigt, wie eine Textzeile mithilfe ihrer Schriftarteigenschaft formatiert wird.

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
