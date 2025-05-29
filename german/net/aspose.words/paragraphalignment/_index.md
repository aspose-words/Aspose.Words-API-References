---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.ParagraphAlignment für eine präzise Textausrichtung in Ihren Dokumenten. Verbessern Sie mühelos Lesbarkeit und Formatierung!
type: docs
weight: 5130
url: /de/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Gibt die Textausrichtung in einem Absatz an.

```csharp
public enum ParagraphAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Left | `0` | Der Text ist linksbündig ausgerichtet. |
| Center | `1` | Der Text wird horizontal zentriert. |
| Right | `2` | Der Text ist rechtsbündig ausgerichtet. |
| Justify | `3` | Der Text wird sowohl links- als auch rechtsbündig ausgerichtet. |
| Distributed | `4` | Der Text ist gleichmäßig verteilt. |
| ArabicMediumKashida | `5` | Nur Arabisch. Die Kashida-Länge für Text wird auf eine vom Benutzer festgelegte mittlere Länge erweitert. |
| ArabicHighKashida | `7` | Nur Arabisch. Die Kashida-Länge für Text wird auf die größtmögliche Länge erweitert. |
| ArabicLowKashida | `8` | Nur Arabisch. Die Kashida-Länge für Text wird auf eine etwas längere Länge erweitert. |
| ThaiDistributed | `9` | Nur Thai. Der Text wird mit einer Optimierung für Thai ausgerichtet. |
| MathElementCenterAsGroup | `10` | Das einzige mathematische Element in einer Zeile, ausgerichtet als „Zentriert als Gruppe“. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
