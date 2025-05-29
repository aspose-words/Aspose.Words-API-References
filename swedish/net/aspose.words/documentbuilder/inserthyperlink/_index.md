---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words för .NET
description: Förbättra dina dokument med DocumentBuilders InsertHyperlink-metod och lägg enkelt till klickbara länkar för förbättrad navigering och användarengagemang.
type: docs
weight: 390
url: /sv/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Infogar en hyperlänk i dokumentet.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| displayText | String | Texten till länken som ska visas i dokumentet. |
| urlOrBookmark | String | Länkdestination. Kan vara en URL eller namnet på ett bokmärke i dokumentet. Den här metoden lägger alltid till apostrofer i början och slutet av URL:en. |
| isBookmark | Boolean | `sann` om föregående parameter är namnet på ett bokmärke i dokumentet; `falsk` är den föregående parametern är en URL. |

### Returvärde

En[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

## Anmärkningar

Observera att du måste ange teckensnittsformatering för hyperlänkens visningstext explicit med hjälp av[`Font`](../font/) egendom.

Denna metod anropar internt[`InsertField`](../insertfield/)för att infoga ett MS Word HYPERLINK field i dokumentet.

## Exempel

Visar hur man infogar ett hyperlänkfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Infoga en hyperlänk och framhäv den med anpassad formatering.
// Hyperlänken kommer att vara en klickbar textbit som tar oss till den plats som anges i URL:en.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falskt);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + vänsterklicka på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Visar hur man infogar en hyperlänk som refererar till ett lokalt bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Infoga ett HYPERLINK-fält som länkar till bokmärket. Vi kan skicka fältväxlar
// till metoden "InsertHyperlink" som en del av argumentet som innehåller det refererade bokmärkets namn.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Visar hur man använder formateringsstack för ett dokumentverktyg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in teckensnittsformatering och skriv sedan texten som kommer före hyperlänken.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Bevara vår nuvarande formateringskonfiguration på stacken.
builder.PushFont();

// Ändra verktygets nuvarande formatering genom att använda en ny stil.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", falskt);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Återställ teckensnittsformateringen som vi sparade tidigare och ta bort elementet från stacken.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
