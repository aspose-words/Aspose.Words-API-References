---
title: SdtType Enum
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Markup.SdtType, die strukturierte Dokument-Tag-Typen für eine verbesserte Dokumentenverwaltung und optimierte Arbeitsabläufe definiert.
type: docs
weight: 4730
url: /de/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Gibt den Typ eines SDT-Knotens (Structured Document Tag) an.

```csharp
public enum SdtType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Dem SDT ist kein Typ zugewiesen. |
| Bibliography | `1` | Das SDT stellt einen Bibliographieeintrag dar. |
| Citation | `2` | Das SDT stellt ein Zitat dar. |
| Equation | `3` | Das SDT stellt eine Gleichung dar. |
| DropDownList | `4` | Das SDT stellt eine Dropdown-Liste dar, wenn es im Dokument angezeigt wird. |
| ComboBox | `5` | Das SDT stellt bei Anzeige im Dokument ein Kombinationsfeld dar. |
| Date | `6` | Das SDT stellt eine Datumsauswahl dar, wenn es im Dokument angezeigt wird. |
| BuildingBlockGallery | `7` | Das SDT stellt einen Bausteingalerietyp dar. |
| DocPartObj | `8` | Das SDT stellt einen Dokumentteiltyp dar. |
| Group | `9` | Das SDT stellt bei der Anzeige im Dokument eine eingeschränkte Gruppierung dar. |
| Picture | `10` | Das SDT stellt ein Bild dar, wenn es im Dokument angezeigt wird. |
| RichText | `11` | Das SDT stellt ein Rich-Text-Feld dar, wenn es im Dokument angezeigt wird. |
| PlainText | `12` | Das SDT stellt bei der Anzeige im Dokument ein einfaches Textfeld dar. |
| Checkbox | `13` | Das SDT stellt ein Kontrollkästchen dar, wenn es im Dokument angezeigt wird. |
| RepeatingSection | `14` | Das SDT stellt den sich wiederholenden Abschnittstyp dar, wenn es im Dokument angezeigt wird. |
| RepeatingSectionItem | `15` | Das SDT stellt ein sich wiederholendes Abschnittselement dar. |
| EntityPicker | `16` | Das SDT stellt einen Entitätswähler dar, der es dem Benutzer ermöglicht, eine Instanz eines externen Inhaltstyps auszuwählen. |

## Beispiele

Zeigt, wie ein strukturiertes Dokument-Tag vom Typ „Zitat“ erstellt wird.

```csharp
Document doc = new Document();

StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.Citation, MarkupLevel.Inline);
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
paragraph.AppendChild(sdt);

// Erstellen Sie ein Zitatfeld.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToParagraph(0, -1);
builder.InsertField(@"CITATION Ath22 \l 1033 ", "(John Lennon, 2022)");

// Verschieben Sie das Feld in das strukturierte Dokument-Tag.
while (sdt.NextSibling != null)
    sdt.AppendChild(sdt.NextSibling);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Citation.docx");
```

Zeigt, wie gruppenstrukturierte Dokument-Tags auf Zeilenebene erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Erstellen Sie auf Zeilenebene ein gruppenstrukturiertes Dokument-Tag.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// Erstellen Sie eine untergeordnete Zeile des strukturierten Dokument-Tags.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// Zelleninhalt einfügen.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// Text nach der Tabelle einfügen.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

Zeigt, wie mit Stilen für Inhaltssteuerelemente gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten finden Sie zwei Möglichkeiten, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 – Wenden Sie ein Stilobjekt aus der Stilsammlung des Dokuments an:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Verweisen Sie im Dokument anhand des Namens auf einen Stil:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

Zeigt, wie eine Tabelle mit Daten aus einem XML-Teil gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>");

// Header für Daten aus dem XML-Inhalt erstellen.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// Erstellen Sie eine Tabelle mit einem sich wiederholenden Abschnitt darin.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Fügen Sie innerhalb des sich wiederholenden Abschnitts ein sich wiederholendes Abschnittselement hinzu und markieren Sie es als Zeile.
// Diese Tabelle enthält eine Zeile für jedes Element, das wir im XML-Dokument finden können
// unter Verwendung des XPath "/books[1]/book", von denen es drei gibt.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Ordnen Sie XML-Daten mit erstellten Tabellenzellen für den Titel und den Autor jedes Buches zu.
StructuredDocumentTag titleSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", string.Empty);
row.AppendChild(titleSdt);

StructuredDocumentTag authorSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", string.Empty);
row.AppendChild(authorSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.RepeatingSectionItem.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
