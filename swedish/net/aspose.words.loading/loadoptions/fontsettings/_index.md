---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words för .NET
description: Anpassa ditt dokuments teckensnittsinställningar med LoadOptions FontSettings för förbättrad läsbarhet och stil. Optimera dina dokument utan ansträngning!
type: docs
weight: 60
url: /sv/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Gör det möjligt att ange dokumentets teckensnittsinställningar.

```csharp
public FontSettings FontSettings { get; set; }
```

## Anmärkningar

När vissa format laddas kan Aspose.Words behöva matcha teckensnitten. Till exempel, när du laddar HTML-dokument kan Aspose.Words matcha teckensnitten för att utföra reservteckensnitt.

Om inställd på`null` , standardinställningar för statiska teckensnitt[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) kommer att användas.

Standardvärdet är`null`.

## Exempel

Visar hur man använder inställningar för teckensnittsersättning när man laddar ett dokument.

```csharp
// Skapa ett FontSettings-objekt som ersätter typsnittet "Times New Roman"
// med typsnittet "Arvo" från vår mapp "MyFonts".
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Ange FontSettings-objektet som en egenskap för ett nyskapat LoadOptions-objekt.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Ladda dokumentet och rendera det sedan som en PDF med teckensnittsersättningen.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Visar hur man anger teckensnittsersättningar under inläsning.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Ange en regel för teckensnittsersättning för ett LoadOptions-objekt.
// Om dokumentet vi laddar använder ett teckensnitt som vi inte har,
// den här regeln kommer att ersätta det otillgängliga teckensnittet med ett som redan finns.
// I det här fallet kommer all användning av "MissingFont" att konverteras till "Comic Sans MS".
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// Vid denna tidpunkt kommer sådan text fortfarande att vara i "MissingFont".
// Typsnittsersättning kommer att ske när vi renderar dokumentet.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Se även

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
