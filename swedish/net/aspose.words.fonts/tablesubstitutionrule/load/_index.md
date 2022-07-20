---
title: Load
second_title: Aspose.Words för .NET API Referens
description: Laddar tabellersättningsinställningar från XML-fil.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/load/
---
## Load(string) {#load_1}

Laddar tabellersättningsinställningar från XML-fil.

```csharp
public void Load(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Inmatat filnamn. |

### Exempel

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

* class [TableSubstitutionRule](../../tablesubstitutionrule)
* namnutrymme [Aspose.Words.Fonts](../../tablesubstitutionrule)
* hopsättning [Aspose.Words](../../../)

---

## Load(Stream) {#load}

Laddar inställningar för tabellersättning från XML-ström.

```csharp
public void Load(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Ingångsström. |

### Exempel

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

* class [TableSubstitutionRule](../../tablesubstitutionrule)
* namnutrymme [Aspose.Words.Fonts](../../tablesubstitutionrule)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
