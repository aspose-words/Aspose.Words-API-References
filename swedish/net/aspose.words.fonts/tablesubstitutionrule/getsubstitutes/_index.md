---
title: TableSubstitutionRule.GetSubstitutes
linktitle: GetSubstitutes
articleTitle: GetSubstitutes
second_title: Aspose.Words för .NET
description: Upptäck GetSubstitutes-metoden i TableSubstitutionRule. Hämta enkelt ersättningsnamn för ditt ursprungliga typsnitt, vilket ökar designflexibiliteten.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/getsubstitutes/
---
## TableSubstitutionRule.GetSubstitutes method

Returnerar en array som innehåller ersättningsnamn för det angivna ursprungliga typsnittsnamnet.

```csharp
public IEnumerable<string> GetSubstitutes(string originalFontName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| originalFontName | String | Ursprungligt typsnittsnamn. |

### Returvärde

Lista över alternativa typsnittsnamn.

## Exempel

Visar hur man kommer åt ett dokuments systemfontkälla och ställer in fontersättningar.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Som standard innehåller ett tomt dokument alltid en systemfontkälla.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Ställ in ett teckensnitt som finns i Windows Fonts-katalogen som ersättning för ett som inte finns.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternativt kan vi lägga till en mapp för teckensnittskälla där motsvarande mapp innehåller teckensnittet.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Om vi återställer teckensnittskällorna har vi fortfarande kvar systemets teckensnittskälla samt våra ersättningar.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
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
