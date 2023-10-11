---
title: Enum SdtType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Markup.SdtType enum. Specifica il tipo di nodo di un tag di documento strutturato SDT.
type: docs
weight: 4040
url: /it/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Specifica il tipo di nodo di un tag di documento strutturato (SDT).

```csharp
public enum SdtType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessun tipo assegnato all'SDT. |
| Bibliography | `1` | L'SDT rappresenta una voce bibliografica. |
| Citation | `2` | L'SDT rappresenta una citazione. |
| Equation | `3` | L'SDT rappresenta un'equazione. |
| DropDownList | `4` | L'SDT rappresenta un elenco a discesa quando viene visualizzato nel documento. |
| ComboBox | `5` | L'SDT rappresenta una casella combinata quando viene visualizzato nel documento. |
| Date | `6` | L'SDT rappresenta un selettore di data quando viene visualizzato nel documento. |
| BuildingBlockGallery | `7` | L'SDT rappresenta un tipo di galleria di blocchi predefiniti. |
| DocPartObj | `8` | L'SDT rappresenta un tipo di parte del documento. |
| Group | `9` | L'SDT rappresenta un raggruppamento ristretto quando visualizzato nel documento. |
| Picture | `10` | L'SDT rappresenta un'immagine quando viene visualizzata nel documento. |
| RichText | `11` | L'SDT rappresenta una casella di testo avanzata quando viene visualizzata nel documento. |
| PlainText | `12` | L'SDT rappresenta una casella di testo semplice quando viene visualizzata nel documento. |
| Checkbox | `13` | L'SDT rappresenta una casella di controllo quando viene visualizzato nel documento. |
| RepeatingSection | `14` | L'SDT rappresenta il tipo di sezione ripetuta quando viene visualizzato nel documento. |
| RepeatingSectionItem | `15` | L'SDT rappresenta l'elemento della sezione ripetuto. |
| EntityPicker | `16` | L'SDT rappresenta un selettore di entità che consente all'utente di selezionare un'istanza di un tipo di contenuto esterno. |

### Esempi

Mostra come creare tag di documento strutturato di gruppo a livello di riga.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Crea un tag di documento strutturato di gruppo a livello di riga.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// Crea una riga secondaria del tag del documento strutturato.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// Inserisci il contenuto della cella.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// Inserisci il testo dopo la tabella.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

Mostra come utilizzare gli stili per gli elementi di controllo del contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 - Applica un oggetto di stile dalla raccolta di stili del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Fa riferimento a uno stile nel documento per nome:
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

Mostra come riempire una tabella con i dati da una parte XML.

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

// Aggiungi l'elemento della sezione ripetuta all'interno della sezione ripetuta e contrassegnalo come riga.
// Questa tabella avrà una riga per ogni elemento che possiamo trovare nel documento XML
// utilizzando l'XPath "/books[1]/book", di cui ce ne sono tre.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Mappa i dati XML con le celle della tabella create per il titolo e l'autore di ciascun libro.
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


