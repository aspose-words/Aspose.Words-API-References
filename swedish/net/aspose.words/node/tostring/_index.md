---
title: ToString
second_title: Aspose.Words för .NET API Referens
description: Exporterar innehållet i noden till en sträng i angivet format.
type: docs
weight: 160
url: /sv/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

Exporterar innehållet i noden till en sträng i angivet format.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Returvärde

Innehållet i noden i det angivna formatet.

### Exempel

Visar skillnaden mellan att anropa GetText- och ToString-metoderna på en nod.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText kommer att hämta den synliga texten samt fältkoder och specialtecken.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString kommer att ge oss dokumentets utseende om det sparas i ett godkänt sparaformat.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Exporterar innehållet i en nod till String i HTML-format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// När vi anropar ToString-metoden med hjälp av html SaveFormat-överbelastningen,
// den konverterar nodens innehåll till deras råa html-representation.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Vi kan också modifiera resultatet av denna konvertering med hjälp av ett SaveOptions-objekt.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

Visar hur man extraherar listetiketterna för alla stycken som är listobjekt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Hitta om vi har styckelistan. I vårt dokument använder vår lista vanliga arabiska siffror,
// som börjar vid tre och slutar vid sex.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Det här är texten vi får när vi matar ut den här noden till textformat.
    // Denna textutgång kommer att utelämna listetiketter. Trimma alla tecken i styckeformatering. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Detta får styckets position på den aktuella nivån i listan. Om vi har en lista med flera nivåer,
    // detta kommer att berätta vilken position det är på den nivån.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Kombinera dem för att inkludera listetiketten med texten i utdata.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Se även

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* namnutrymme [Aspose.Words](../../node/)
* hopsättning [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

Exporterar innehållet i noden till en sträng med de angivna sparalternativen.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveOptions | SaveOptions | Anger alternativen som styr hur noden sparas. |

### Returvärde

Innehållet i noden i det angivna formatet.

### Exempel

Exporterar innehållet i en nod till String i HTML-format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// När vi anropar ToString-metoden med hjälp av html SaveFormat-överbelastningen,
// den konverterar nodens innehåll till deras råa html-representation.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Vi kan också modifiera resultatet av denna konvertering med hjälp av ett SaveOptions-objekt.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* namnutrymme [Aspose.Words](../../node/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
