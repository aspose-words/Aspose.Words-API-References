---
title: SdtType
second_title: Aspose.Words per .NET API Reference
description: Specifica il tipo di un nodo SDT Structure Document Tag.
type: docs
weight: 3800
url: /it/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Specifica il tipo di un nodo SDT (Structure Document Tag).

```csharp
public enum SdtType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessun tipo è assegnato all'SDT. |
| Bibliography | `1` | L'SDT rappresenta una voce di bibliografia. |
| Citation | `2` | L'SDT rappresenta una citazione. |
| Equation | `3` | L'SDT rappresenta un'equazione. |
| DropDownList | `4` | L'SDT rappresenta un elenco a discesa quando visualizzato nel documento. |
| ComboBox | `5` | L'SDT rappresenta una casella combinata quando viene visualizzato nel documento. |
| Date | `6` | L'SDT rappresenta un selettore di data quando visualizzato nel documento. |
| BuildingBlockGallery | `7` | L'SDT rappresenta un tipo di galleria di blocchi predefiniti. |
| DocPartObj | `8` | L'SDT rappresenta un tipo di parte del documento. |
| Group | `9` | L'SDT rappresenta un raggruppamento limitato quando visualizzato nel documento. |
| Picture | `10` | L'SDT rappresenta un'immagine quando viene visualizzata nel documento. |
| RichText | `11` | L'SDT rappresenta una casella di testo RTF quando visualizzato nel documento. |
| PlainText | `12` | L'SDT rappresenta una casella di testo normale quando visualizzata nel documento. |
| Checkbox | `13` | L'SDT rappresenta una casella di controllo quando viene visualizzato nel documento. |
| RepeatingSection | `14` | L'SDT rappresenta il tipo di sezione ripetuta quando visualizzato nel documento. |
| RepeatingSectionItem | `15` | L'SDT rappresenta l'elemento della sezione ripetuta. |
| EntityPicker | `16` | L'SDT rappresenta un selettore di entità che consente all'utente di selezionare un'istanza di un tipo di contenuto esterno. |

### Esempi

Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 - Applica un oggetto di stile dalla raccolta di stili del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Fai riferimento a uno stile nel documento per nome:
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

Mostra come riempire una tabella con dati da una parte XML.

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

// Crea intestazioni per i dati dal contenuto XML.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// Crea una tabella con una sezione ripetuta all'interno.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Aggiungi l'elemento della sezione ripetuta all'interno della sezione ripetuta e contrassegnalo come una riga.
// Questa tabella avrà una riga per ogni elemento che possiamo trovare nel documento XML
// usando "/books[1]/book" XPath, di cui ce ne sono tre.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Mappa i dati XML con le celle di tabella create per il titolo e l'autore di ogni libro.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
