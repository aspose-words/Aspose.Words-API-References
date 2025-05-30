---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words för .NET
description: Optimera dina HTML-, MHTML- eller EPUB-filer med egenskapen FontResourcesSubsettingSizeThreshold, vilket säkerställer effektiv hantering av teckensnittsresurser. Standardvärde 0.
type: docs
weight: 290
url: /sv/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Styr vilka teckensnittsresurser som behöver delinställningar när man sparar till HTML, MHTML eller EPUB. Standard är`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Anmärkningar

[`ExportFontResources`](../exportfontresources/) tillåter export av teckensnitt som underordnade filer eller som delar av output -paketet. Om dokumentet använder många teckensnitt, särskilt med ett stort antal teckensnitt, kan utdatastorleken öka avsevärt. Teckensnittsunderinställningar minskar storleken på den exporterade teckensnittsresursen genom att filtrera bort teckensnitt som inte används av det aktuella dokumentet.

Delinställning av teckensnitt fungerar så här:

* Som standard är alla exporterade teckensnitt delmängder.
* Miljö`FontResourcesSubsettingSizeThreshold` till ett positivt värde instruerar Aspose.Words att delmängdera teckensnitt vars filstorlek är större än det angivna värdet.
* Ställa in egenskapen tillMaxValue undertrycker delmängder av teckensnitt.

**Viktig!**Vid export av typsnittsresurser bör man beakta frågor om typsnittslicenser. Författare som vill använda specifika typsnitt via en nedladdningsbar typsnittsmekanism måste alltid noggrant kontrollera att deras avsedda användning ligger inom typsnittslicensens omfattning. Många kommersiella typsnitt tillåter för närvarande inte nedladdning av deras typsnitt på webben i någon form. Licensavtal som täcker vissa typsnitt noterar specifikt att användning via**@font-face** rules i CSS-stilmallar är inte tillåtet. Delmängder av teckensnitt kan också bryta mot licensvillkoren.

## Exempel

Visar hur man arbetar med teckensnittsundergrupper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt som konfigurerar font-underinställningen.
// Anta att vi sätter flaggan "ExportFontResources" till "true" och även namnger en mapp i egenskapen "FontsFolder".
// I så fall skapar sparoperationen den mappen och placerar en .ttf-fil inuti
// den mappen för varje teckensnitt som vårt dokument använder.
// Varje .ttf-fil kommer att innehålla hela teckensnittets uppsättning teckensnitt,
// vilket potentiellt kan resultera i en mycket stor fil som medföljer dokumentet.
// När vi använder delmängder på ett teckensnitt kommer dess exporterade rådata endast att innehålla de tecken som dokumentet är
// använder istället för hela teckenuppsättningen. Om texten i vårt dokument bara använder en liten del av ett teckensnitts
// glyfuppsättning, då kommer delmängder att minska storleken på våra utdatadokument avsevärt.
// Vi kan använda egenskapen "FontResourcesSubsettingSizeThreshold" för att definiera en .ttf-filstorlek i byte.
 // Om ett exporterat teckensnitt skapar en större fil än så, kommer sparåtgärden att tillämpa en delmängd på det teckensnittet.
// Om tröskeln 0 sätts gäller delinställningar för alla teckensnitt,
// och att sätta den till "int.MaxValue" inaktiverar effektivt delmängder.
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
    // Som standard kommer .ttf-filerna för vart och ett av våra tre typsnitt att vara över 700 MB.
    // Delmängder minskar dem alla till under 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
