---
title: FontSettings
second_title: Aspose.Words för .NET API Referens
description: Anger teckensnittsinställningar för ett dokument.
type: docs
weight: 2790
url: /sv/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Anger teckensnittsinställningar för ett dokument.

```csharp
public class FontSettings
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FontSettings](fontsettings)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance) { get; } | Statiska standardteckensnittsinställningar. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings) { get; } | Inställningar relaterade till reservmekanism för teckensnitt. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings) { get; } | Inställningar relaterade till teckensnittsersättningsmekanism. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources)() | Får en kopia av arrayen som innehåller listan över källor där Aspose.Words letar efter TrueType-teckensnitt. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources)() | Återställer teckensnittskällorna till systemets standard. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache)(Stream) | Sparar typsnittssökningscachen i strömmen. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder)(string, bool) | Ställer in mappen där Aspose.Words söker efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt. Detta är en genväg till[`SetFontsFolders`](./setfontsfolders) för att endast ställa in en teckensnittskatalog. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders)(string[], bool) | Ställer in mapparna där Aspose.Words söker efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources#setfontssources)(FontSourceBase[]) | Ställer in källorna där Aspose.Words söker efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources#setfontssources_1)(FontSourceBase[], Stream) | Ställer in källorna där Aspose.Words söker efter TrueType-teckensnitt och laddar dessutom tidigare sparad typsnittssökningscache. |

### Anmärkningar

Aspose.Words använder teckensnittsinställningar för att lösa teckensnitten i dokumentet. Teckensnitt löses mest när man bygger dokumentlayout eller renderar till fasta sidformat. Men när du laddar vissa format kan Aspose.Words också behöva lösa teckensnitten. Till exempel, när laddar HTML-dokument Aspose.Words kan lösa teckensnitten för att utföra fallback. Så det rekommenderas att du ställer in teckensnittsinställningarna i [`LoadOptions`](../../aspose.words.loading/loadoptions) när du laddar dokumentet. Eller åtminstone innan du bygger layouten eller renderar dokumentet till formatet med fasta sidor.

Som standard använder alla dokument enstaka statiska teckensnittsinställningar. Den kunde nås av [`DefaultInstance`](./defaultinstance) fast egendom.

Att ändra teckensnittsinställningar är säkert när som helst från vilken tråd som helst. Men det rekommenderas att du inte ändrar teckensnittsinställningarna medan bearbetar vissa dokument som använder dessa inställningar. Detta kan leda till att samma typsnitt kommer att lösas olika i olika delar av dokumentet.

### Exempel

Visar hur du lägger till en teckensnittskälla till våra befintliga teckensnittskällor.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardfontkällan saknar två av de teckensnitt som vi använder i vårt dokument.
// När vi sparar det här dokumentet kommer Aspose.Words att tillämpa reservteckensnitt på all text som är formaterad med otillgängliga teckensnitt.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Skapa en teckensnittskälla från en mapp som innehåller teckensnitt.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Använd en ny uppsättning teckensnittskällor som innehåller de ursprungliga teckensnittskällorna, såväl som våra anpassade teckensnitt.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verifiera att Aspose.Words har tillgång till alla nödvändiga teckensnitt innan vi renderar dokumentet till PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Återställ de ursprungliga teckensnittskällorna.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Visar hur man ställer in en teckensnittskällkatalog.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Våra teckensnittskällor innehåller inte det teckensnitt som vi har använt för text i detta dokument.
// Om vi använder dessa teckensnittsinställningar när vi renderar detta dokument,
// Aspose.Words kommer att tillämpa ett reservteckensnitt på text som har ett teckensnitt som Aspose.Words inte kan hitta.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardteckensnittskällorna saknar de två typsnitten som vi använder i det här dokumentet.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Använd metoden "SetFontsFolder" för att ställa in en katalog som kommer att fungera som en ny teckensnittskälla.
// Skicka "false" som det "rekursiva" argumentet för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogen
// som vi skickar i det första argumentet, men inte inkluderar några teckensnitt i någon av den katalogens undermappar.
// Skicka "true" som det "rekursiva" argumentet för att inkludera alla teckensnittsfiler i katalogen som vi skickar
// i det första argumentet, såväl som alla teckensnitt i dess underkataloger.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Teckensnittet "Amethysta" finns i en undermapp till teckensnittskatalogen.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Återställ de ursprungliga teckensnittskällorna.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Visar hur du ställer in flera teckensnittskataloger.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Våra teckensnittskällor innehåller inte det teckensnitt som vi har använt för text i detta dokument.
// Om vi använder dessa teckensnittsinställningar när vi renderar detta dokument,
// Aspose.Words kommer att tillämpa ett reservteckensnitt på text som har ett teckensnitt som Aspose.Words inte kan hitta.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardteckensnittskällorna saknar de två typsnitten som vi använder i det här dokumentet.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Använd metoden "SetFontsFolders" för att skapa en teckensnittskälla från varje teckensnittskatalog som vi skickar som det första argumentet.
// Skicka "false" som det "rekursiva" argumentet för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogerna
// att vi skickar i det första argumentet, men inte inkluderar några typsnitt från någon av katalogernas undermappar.
// Ange "true" som det "rekursiva" argumentet för att inkludera alla teckensnittsfiler i katalogerna som vi skickar
// i det första argumentet, såväl som alla teckensnitt i deras underkataloger.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Själva mappen "Junction" innehåller inga teckensnittsfiler, men har undermappar som gör det.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Återställ de ursprungliga teckensnittskällorna.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Se även

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
