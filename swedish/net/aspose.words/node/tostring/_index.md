---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words för .NET
description: Upptäck Node ToString-metoden, konvertera enkelt nodinnehåll till strängar med anpassningsbara format för förbättrad datahantering. Optimera din kodning idag!
type: docs
weight: 160
url: /sv/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Exporterar nodens innehåll till en sträng i det angivna formatet.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Returvärde

Nodens innehåll i det angivna formatet.

## Exempel

Visar skillnaden mellan att anropa GetText- och ToString-metoderna på en nod.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText hämtar den synliga texten samt fältkoder och specialtecken.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString ger oss dokumentets utseende om det sparas i ett godkänt format.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Exporterar innehållet i en nod till en sträng i HTML-format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// När vi anropar ToString-metoden med hjälp av html SaveFormat-överbelastningen,
// den konverterar nodens innehåll till dess råa html-representation.
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

// Se om vi har styckelistan. I vårt dokument använder vår lista vanliga arabiska siffror,
// som börjar vid tre och slutar vid sex.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Detta är texten vi får när vi skriver ut noden i textformat.
     // Denna textutdata kommer att utelämna listetiketter. Beskär alla tecken för styckeformatering.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Detta hämtar styckets position på listans aktuella nivå. Om vi har en lista med flera nivåer,
    // detta kommer att berätta för oss vilken position den är på den nivån.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Kombinera dem för att inkludera listetiketten med texten i utdata.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Se även

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Exporterar nodens innehåll till en sträng med de angivna sparalternativen.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveOptions | SaveOptions | Anger de alternativ som styr hur noden sparas. |

### Returvärde

Nodens innehåll i det angivna formatet.

## Exempel

Exporterar innehållet i en nod till en sträng i HTML-format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// När vi anropar ToString-metoden med hjälp av html SaveFormat-överbelastningen,
// den konverterar nodens innehåll till dess råa html-representation.
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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
