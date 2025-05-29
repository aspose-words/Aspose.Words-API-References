---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar typsnittsnamn med metoden TableSubstitutionRule SetSubstitutes. Förbättra din design med skräddarsydda typografilösningar!
type: docs
weight: 80
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Åsidosätt ersättningsteckensnittsnamn för angivet originalteckensnittsnamn.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| originalFontName | String | Ursprungligt typsnittsnamn. |
| substituteFontNames | String[] | Lista över alternativa typsnittsnamn. |

## Exempel

Visar hur man ställer in regler för teckensnittsersättning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Standardfontkällorna innehåller det första font som dokumentet använder.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Det andra typsnittet, "Amethysta", är inte tillgängligt.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Vi kan konfigurera en tabell för typsnittsersättning som bestämmer
// vilka typsnitt Aspose.Words kommer att använda som ersättning för otillgängliga typsnitt.
// Ställ in två ersättningsfonter för "Amethysta": "Arvo" och "Courier New".
// Om den första ersättningen inte är tillgänglig försöker Aspose.Words använda den andra ersättningen, och så vidare.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" är inte tillgängligt, och substitutionsregeln anger att det första teckensnittet som ska användas som ersättning är "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" är inte heller tillgängligt, men det är "Courier New".
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Utdatadokumentet visar texten som använder teckensnittet "Amethysta" formaterat med "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Visar hur man arbetar med anpassade teckensnittsersättningstabeller.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Skapa en ny regel för tabellersättning och ladda standardtabellen för Windows-teckensnittsersättning.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Om vi väljer teckensnitt uteslutande från vår mapp behöver vi en anpassad ersättningstabell.
// Vi kommer inte längre att ha tillgång till Microsoft Windows-teckensnitten,
// som till exempel "Arial" eller "Times New Roman" eftersom de inte finns i vår nya typsnittsmapp.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Nedan följer två sätt att ladda en substitutionstabell från en fil i det lokala filsystemet.
// 1 - Från en ström:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Direkt från en fil:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Eftersom vi inte längre har tillgång till "Arial" kommer vår typsnittstabell först att försöka ersätta den med "Icke-existerande typsnitt".
// Vi har inte det här typsnittet så det kommer att flyttas till nästa ersättningstypsnitt, "Kreon", som finns i mappen "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Vi kan expandera den här tabellen programmatiskt. Vi lägger till en post som ersätter "Times New Roman" med "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Vi kan lägga till en sekundär reserversättning för en befintlig typsnittspost med AddSubstitutes().
// Om "Arvo" inte är tillgängligt kommer vår tabell att leta efter "M+ 2m" som ett andra alternativ.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() kan ange en ny lista med ersättningsfonter för ett font.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Att skriva text i teckensnitt som vi inte har tillgång till kommer att aktivera våra ersättningsregler.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Se även

* class [TableSubstitutionRule](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
