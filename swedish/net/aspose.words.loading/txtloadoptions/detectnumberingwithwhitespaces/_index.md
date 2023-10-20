---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words för .NET
description: TxtLoadOptions DetectNumberingWithWhitespaces fast egendom. Gör det möjligt att ange hur numrerade listobjekt ska kännas igen när dokument importeras från vanligt textformat. Standardvärdet ärSann i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Gör det möjligt att ange hur numrerade listobjekt ska kännas igen när dokument importeras från vanligt textformat. Standardvärdet är`Sann`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Anmärkningar

Om det här alternativet är inställt på`falsk`, listigenkänningsalgoritm upptäcker liststycken, när listnummer slutar med antingen punkt-, högerparentes eller punktsymboler (som "•", "*", "-" eller "o").

Om det här alternativet är inställt på`Sann`blanksteg används också som listnummeravgränsare: listigenkänningsalgoritm för numrering i arabisk stil (1., 1.1.2.) använder både blanksteg och punktsymboler (".").

## Exempel

Visar hur man upptäcker listor vid inläsning av klartextdokument.

```csharp
// Skapa ett klartextdokument i en sträng med fyra separata delar som vi kan tolka som listor,
// med olika avgränsare. När du laddar klartextdokumentet i ett "Dokument"-objekt,
// Aspose.Words kommer alltid att upptäcka de tre första listorna och lägger till ett "List"-objekt
// för varje till dokumentets "Lists"-egenskap.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett dokument i klartext.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Ställ in egenskapen "DetectNumberingWithWhitespaces" till "true" för att upptäcka numrerade objekt
// med blankstegsavgränsare, som den fjärde listan i vårt dokument, som listor.
// Detta kan också felaktigt upptäcka stycken som börjar med siffror som listor.
// Ställ in egenskapen "DetectNumberingWithWhitespaces" till "false"
// för att inte skapa listor från numrerade objekt med blankstegsavgränsare.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### Se även

* class [TxtLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
