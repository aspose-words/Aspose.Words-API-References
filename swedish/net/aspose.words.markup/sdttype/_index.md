---
title: SdtType
second_title: Aspose.Words för .NET API Referens
description: Anger typen av en strukturerad dokumenttagg SDTnod.
type: docs
weight: 3800
url: /sv/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Anger typen av en strukturerad dokumenttagg (SDT)-nod.

```csharp
public enum SdtType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Ingen typ har tilldelats SDT. |
| Bibliography | `1` | SDT representerar en bibliografipost. |
| Citation | `2` | SDT representerar ett citat. |
| Equation | `3` | SDT representerar en ekvation. |
| DropDownList | `4` | SDT representerar en rullgardinslista när den visas i dokumentet. |
| ComboBox | `5` | SDT representerar en kombinationsruta när den visas i dokumentet. |
| Date | `6` | SDT representerar en datumväljare när den visas i dokumentet. |
| BuildingBlockGallery | `7` | SDT representerar en byggstensgallerityp. |
| DocPartObj | `8` | SDT representerar en dokumentdeltyp. |
| Group | `9` | SDT representerar en begränsad gruppering när den visas i dokumentet. |
| Picture | `10` | SDT representerar en bild när den visas i dokumentet. |
| RichText | `11` | SDT representerar en rik textruta när den visas i dokumentet. |
| PlainText | `12` | SDT representerar en vanlig textruta när den visas i dokumentet. |
| Checkbox | `13` | SDT representerar en kryssruta när den visas i dokumentet. |
| RepeatingSection | `14` | SDT representerar repeterande sektionstyp när den visas i dokumentet. |
| RepeatingSectionItem | `15` | SDT representerar repeterande sektionsobjekt. |
| EntityPicker | `16` | SDT representerar en enhetsväljare som låter användaren välja en instans av en extern innehållstyp. |

### Exempel

Visar hur man arbetar med stilar för innehållskontrollelement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två sätt att tillämpa en stil från dokumentet på en strukturerad dokumenttagg.
// 1 - Använd ett stilobjekt från dokumentets stilsamling:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Referera till en stil i dokumentet efter namn:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

Visar hur man fyller en tabell med data från en XML-del.

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

// Skapa rubriker för data från XML-innehållet.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// Skapa en tabell med ett upprepande avsnitt inuti.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Lägg till ett repeterande avsnitt i det upprepade avsnittet och markera det som en rad.
// Den här tabellen kommer att ha en rad för varje element som vi kan hitta i XML-dokumentet
// med "/books[1]/book" XPath, av vilka det finns tre.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Mappa XML-data med skapade tabellceller för titeln och författaren till varje bok.
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

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
