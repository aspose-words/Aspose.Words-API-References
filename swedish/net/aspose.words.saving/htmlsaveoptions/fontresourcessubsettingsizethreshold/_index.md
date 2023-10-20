---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words för .NET
description: HtmlSaveOptions FontResourcesSubsettingSizeThreshold fast egendom. Styr vilka teckensnittsresurser som behöver underinställning när du sparar till HTML MHTML eller EPUB. Standard är0  i C#.
type: docs
weight: 290
url: /sv/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Styr vilka teckensnittsresurser som behöver underinställning när du sparar till HTML, MHTML eller EPUB. Standard är`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Anmärkningar

[`ExportFontResources`](../exportfontresources/) tillåter export av teckensnitt som underordnade filer eller som delar av paketet output . Om dokumentet använder många teckensnitt, särskilt med ett stort antal glyfer, kan utdatastorleken växa avsevärt. Teckensnittsunderinställning minskar storleken på den exporterade teckensnittsresursen genom att filtrera bort glyfer som inte används av det aktuella dokumentet.

Teckensnittsunderinställning fungerar enligt följande:

* Som standard är alla exporterade teckensnitt underuppsättningar.
* Miljö`FontResourcesSubsettingSizeThreshold`till ett positivt värde instruerar Aspose.Words att underställa teckensnitt vars filstorlek är större än det angivna värdet.
* Ställer in fastigheten tillMaxValue undertrycker teckensnittsunderinställningar.

**Viktig!** När du exporterar teckensnittsresurser bör teckensnittslicensproblem övervägas. Författare som vill använda specifika typsnitt via en nedladdningsbar teckensnittsmekanism måste alltid noggrant verifiera att deras avsedda användning ligger inom ramen för teckensnittslicensen. Många kommersiella typsnitt tillåter för närvarande inte webbnedladdning av deras typsnitt i någon form. Licensavtal som täcker vissa typsnitt noterar specifikt att användning via**@font-face** rules i CSS-formatmallar är inte tillåtet. Teckensnittsunderinställningar kan också bryta mot licensvillkoren.

## Exempel

Visar hur man arbetar med teckensnittsunderinställningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// När vi sparar dokumentet till HTML, kan vi skicka en SaveOptions-objektkonfigurering av teckensnitt.
// Anta att vi ställer in flaggan "ExportFontResources" till "true" och även namnger en mapp i egenskapen "FontsFolder".
// I så fall kommer sparoperationen att skapa den mappen och placera en .ttf-fil inuti
// den mappen för varje typsnitt som vårt dokument använder.
// Varje .ttf-fil kommer att innehålla teckensnittets hela teckenuppsättning,
// vilket potentiellt kan resultera i en mycket stor fil som åtföljer dokumentet.
// När vi tillämpar underinställning på ett teckensnitt kommer dess exporterade rådata bara att innehålla de glyfer som dokumentet är
// använder istället för hela glyph-uppsättningen. Om texten i vårt dokument bara använder en liten bråkdel av ett teckensnitt
// glyph set, då kommer underinställningar att minska storleken på våra utdatadokument avsevärt.
// Vi kan använda egenskapen "FontResourcesSubsettingSizeThreshold" för att definiera en .ttf-filstorlek, i byte.
 // Om ett exporterat teckensnitt skapar en fil som är större än så, kommer spara-operationen att tillämpa underinställningar på det teckensnittet.
// Om du ställer in ett tröskelvärde på 0 tillämpas underinställning på alla teckensnitt,
// och ställer in den till "int.MaxValue" inaktiverar effektivt delinställningar.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // Som standard kommer .ttf-filerna för vart och ett av våra tre teckensnitt att vara över 700 MB.
    // Underinställning minskar alla till under 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
