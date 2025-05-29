---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words för .NET
description: Upptäck metoden FontSettings GetFontsSources för att enkelt komma åt en mängd olika källor för TrueType-teckensnitt i Aspose.Words. Optimera din teckensnittshantering idag!
type: docs
weight: 50
url: /sv/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Hämtar en kopia av arrayen som innehåller listan över källor där Aspose.Words letar efter TrueType-teckensnitt.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Returvärde

En kopia av de aktuella teckensnittskällorna.

## Anmärkningar

Det returnerade värdet är en kopia av de data som Aspose.Words använder. Om du ändrar entries i den returnerade arrayen kommer det inte att ha någon effekt på dokumentrenderingen. För att ange nya teckensnittskällor , använd[`SetFontsSources`](../setfontssources/) metod.

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

### Se även

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
