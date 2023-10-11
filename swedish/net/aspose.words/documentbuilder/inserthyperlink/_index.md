---
title: DocumentBuilder.InsertHyperlink
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Infogar en hyperlänk i dokumentet.
type: docs
weight: 370
url: /sv/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Infogar en hyperlänk i dokumentet.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| displayText | String | Text till länken som ska visas i dokumentet. |
| urlOrBookmark | String | Länkdestination. Kan vara en webbadress eller ett namn på ett bokmärke inuti dokumentet. Denna metod lägger alltid till apostrof i början och slutet av webbadressen. |
| isBookmark | Boolean | `Sann` om den föregående parametern är ett namn på ett bokmärke i dokumentet; `falsk` är den föregående parametern är en URL. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

### Anmärkningar

Observera att du måste ange teckensnittsformatering för hyperlänkens visningstext explicit med hjälp av[`Font`](../font/) fast egendom.

Denna metod anropar internt[`InsertField`](../insertfield/) för att infoga ett MS Word HYPERLINK-fält i dokumentet.

### Exempel

Visar hur man infogar en hyperlänk som refererar till ett lokalt bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Infoga ett HYPERLÄNK-fält som länkar till bokmärket. Vi kan passera fältväxlar
// till metoden "InsertHyperlink" som en del av argumentet som innehåller det refererade bokmärkets namn.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Visar hur man infogar ett hyperlänkfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Infoga en hyperlänk och framhäva den med anpassad formatering.
// Hyperlänken kommer att vara ett klickbart stycke text som tar oss till den plats som anges i URL:en.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + vänsterklicka på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Visar hur du använder en dokumentbyggares formateringsstack.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in teckensnittsformatering och skriv sedan texten som går före hyperlänken.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Bevara vår nuvarande formateringskonfiguration i stacken.
builder.PushFont();

// Ändra byggarens nuvarande formatering genom att använda en ny stil.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

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
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


