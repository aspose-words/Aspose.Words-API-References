---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: Aspose.Words för .NET
description: TableSubstitutionRule SetSubstitutes metod. Åsidosätt ersättande teckensnittsnamn för det ursprungliga teckensnittsnamnet i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Åsidosätt ersättande teckensnittsnamn för det ursprungliga teckensnittsnamnet.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| originalFontName | String | Ursprungligt teckensnittsnamn. |
| substituteFontNames | String[] | Lista över alternativa teckensnittsnamn. |

## Exempel

Visar hur du ställer in regler för teckensnittsersättning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Standardteckensnittskällorna innehåller det första teckensnittet som dokumentet använder.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Det andra teckensnittet, "Amethysta", är inte tillgängligt.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Vi kan konfigurera en teckensnittsersättningstabell som avgör
// vilka typsnitt Aspose.Words kommer att använda som ersättning för otillgängliga teckensnitt.
// Ställ in två ersättningsteckensnitt för "Amethysta": "Arvo" och "Courier New".
// Om den första ersättningen inte är tillgänglig försöker Aspose.Words använda den andra ersättningen och så vidare.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" är inte tillgängligt, och substitutionsregeln säger att det första teckensnittet som används som ersättning är "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" är inte heller tillgänglig, men "Courier New" är det.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Utdatadokumentet kommer att visa texten som använder "Amethysta"-teckensnittet formaterat med "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Visar hur man arbetar med anpassade teckensnittsersättningstabeller.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Skapa en ny regel för tabellersättning och ladda standardtabellen för Windows-typsnittsersättning.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Om vi väljer typsnitt uteslutande från vår mapp behöver vi en anpassad ersättningstabell.
// Vi kommer inte längre att ha tillgång till Microsoft Windows-teckensnitten,
// som "Arial" eller "Times New Roman" eftersom de inte finns i vår nya typsnittsmapp.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Nedan finns två sätt att ladda en ersättningstabell från en fil i det lokala filsystemet.
// 1 - Från en ström:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Direkt från en fil:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Eftersom vi inte längre har tillgång till "Arial", kommer vår teckensnittstabell först att försöka ersätta den med "Ickeexisterande teckensnitt".
// Vi har inte det här typsnittet så att det kommer att flyttas till nästa ersättning, "Kreon", som finns i mappen "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Vi kan utöka den här tabellen programmatiskt. Vi kommer att lägga till en post som ersätter "Times New Roman" med "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Vi kan lägga till en sekundär reserversättning för en befintlig teckensnittspost med AddSubstitutes().
// Om "Arvo" inte är tillgänglig, kommer vår tabell att leta efter "M+ 2m" som ett andra alternativ.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() kan ställa in en ny lista med ersättningsteckensnitt för ett teckensnitt.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Att skriva text i typsnitt som vi inte har tillgång till kommer att åberopa våra ersättningsregler.
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
