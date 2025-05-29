---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FontSettings för att enkelt anpassa dokumentteckensnittsinställningar för förbättrad läsbarhet och professionell presentation.
type: docs
weight: 3400
url: /sv/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Anger teckensnittsinställningar för ett dokument.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FontSettings
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FontSettings](fontsettings/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Statiska standardinställningar för teckensnitt. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Inställningar relaterade till alternativ mekanism för teckensnitt. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Inställningar relaterade till mekanism för teckensnittsersättning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Hämtar en kopia av arrayen som innehåller listan över källor där Aspose.Words letar efter TrueType-teckensnitt. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Återställer teckensnittskällorna till systemets standardinställningar. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | Sparar cachen för teckensnittssökning i strömmen. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | Anger mappen där Aspose.Words letar efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt. Detta är en genväg till[`SetFontsFolders`](./setfontsfolders/) för att endast ställa in en typsnittskatalog. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | Anger mapparna där Aspose.Words letar efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | Anger källorna där Aspose.Words letar efter TrueType-teckensnitt vid rendering av dokument eller inbäddning av teckensnitt. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | Anger källorna där Aspose.Words söker efter TrueType-teckensnitt och dessutom laddar tidigare sparad cache för teckensnittssökning. |

## Anmärkningar

Aspose.Words använder teckensnittsinställningar för att tolka teckensnitten i dokumentet. Teckensnitt tolkas oftast när man bygger dokumentlayout eller renderar till fasta sidformat. Men när man laddar vissa format kan Aspose.Words också behöva tolka teckensnitten. Till exempel, när laddar HTML-dokument kan Aspose.Words tolka teckensnitten för att utföra reservfunktioner. Så det rekommenderas att du ställer in teckensnittsinställningarna i .[`LoadOptions`](../../aspose.words.loading/loadoptions/) när dokumentet laddas. Eller åtminstone innan layouten skapas eller dokumentet renderas till formatet med fasta sidor.

Som standard använder alla dokument en enda statisk typsnittsinstans. Den kan nås via [`DefaultInstance`](./defaultinstance/) egendom.

Det är säkert att ändra teckensnittsinställningar när som helst från vilken tråd som helst. Men det rekommenderas att du inte ändrar teckensnittsinställningarna medan bearbetar vissa dokument som använder dessa inställningar. Detta kan leda till att samma teckensnitt kommer att upplösas olika i olika delar av dokumentet.

## Exempel

Visar hur man lägger till en teckensnittskälla till våra befintliga teckensnittskällor.

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

// Standardfontkällan saknar två av de fonter som vi använder i vårt dokument.
// När vi sparar det här dokumentet kommer Aspose.Words att använda reservteckensnitt på all text som är formaterad med oåtkomliga teckensnitt.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Skapa en typsnittskälla från en mapp som innehåller typsnitt.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Använd en ny array med teckensnittskällor som innehåller de ursprungliga teckensnittskällorna, såväl som våra anpassade teckensnitt.
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

Visar hur man ställer in en källkatalog för teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Våra typsnittskällor innehåller inte det typsnitt som vi har använt för texten i det här dokumentet.
// Om vi använder dessa teckensnittsinställningar när vi renderar detta dokument,
// Aspose.Words kommer att använda ett reservteckensnitt för text som har ett teckensnitt som Aspose.Words inte kan hitta.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardfontkällorna saknar de två fonter som vi använder i det här dokumentet.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Använd metoden "SetFontsFolder" för att ange en katalog som ska fungera som en ny teckensnittskälla.
// Skicka "false" som argumentet "rekursivt" för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogen
// som vi skickar med i det första argumentet, men inte inkluderar några teckensnitt i någon av undermapparna i den katalogen.
// Skicka "true" som argumentet "rekursivt" för att inkludera alla teckensnittsfiler i den katalog vi skickar
// i det första argumentet, såväl som alla teckensnitt i dess underkataloger.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Typsnittet "Amethysta" finns i en undermapp i typsnittskatalogen.
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

Visar hur man ställer in flera källkataloger för teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Våra typsnittskällor innehåller inte det typsnitt som vi har använt för texten i det här dokumentet.
// Om vi använder dessa teckensnittsinställningar när vi renderar detta dokument,
// Aspose.Words kommer att använda ett reservteckensnitt för text som har ett teckensnitt som Aspose.Words inte kan hitta.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Standardfontkällorna saknar de två fonter som vi använder i det här dokumentet.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Använd metoden "SetFontsFolders" för att skapa en teckensnittskälla från varje teckensnittskatalog som vi skickar som första argument.
// Skicka "false" som argumentet "rekursivt" för att inkludera teckensnitt från alla teckensnittsfiler som finns i katalogerna
// som vi skickar med i det första argumentet, men inte inkluderar några teckensnitt från någon av katalogernas undermappar.
// Skicka "true" som argumentet "rekursivt" för att inkludera alla teckensnittsfiler i de kataloger vi skickar
// i det första argumentet, såväl som alla teckensnitt i deras underkataloger.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Själva mappen "Junction" innehåller inga typsnittsfiler, men har undermappar som gör det.
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

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
