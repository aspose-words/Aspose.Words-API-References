---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words för .NET
description: Kontrollera hyperlänkbeteendet i din PDF med PdfSaveOptions. Ställ enkelt in länkar så att de öppnas i ett nytt fönster eller en ny flik för en förbättrad användarupplevelse.
type: docs
weight: 230
url: /sv/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Hämtar eller anger ett värde som avgör om hyperlänkar i PDF-dokumentet tvingas öppnas i ett nytt fönster (eller en ny flik) i en webbläsare.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` När detta värde är inställt på`sann` hyperlänkar sparas med JavaScript-kod. JavaScript-kod är`app.launchURL("URL", true);` , var`URL` är en hyperlänk.

Observera att om det här alternativet är inställt på`sann` hyperlänkar fungerar inte i vissa PDF-läsare, t.ex. Chrome, Firefox.

JavaScript-åtgärder är förbjudna enligt PDF/A-1- och PDF/A-2-efterlevnad.`falsk`kommer att användas automatiskt när sparas till PDF/A-1 och PDF/A-2.

## Exempel

Visar hur man sparar hyperlänkar i ett dokument som vi konverterar till PDF så att de öppnar nya sidor när vi klickar på dem.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", falskt);

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Sätt egenskapen "OpenHyperlinksInNewWindow" till "true" för att spara alla hyperlänkar med Javascript-kod
// som tvingar läsare att öppna dessa länkar i nya fönster/webbläsarflikar.
// Sätt egenskapen "OpenHyperlinksInNewWindow" till "false" för att spara alla hyperlänkar normalt.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
