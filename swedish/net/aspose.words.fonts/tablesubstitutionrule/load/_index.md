---
title: TableSubstitutionRule.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words för .NET
description: Ladda enkelt in tabellersättningsinställningar från XML-filer med TableSubstitutionRule Load-metoden. Optimera din datahantering idag!
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/tablesubstitutionrule/load/
---
## Load(*string*) {#load_1}

Laddar inställningar för tabellersättning från XML-fil.

```csharp
public void Load(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Inmatningsfilnamn. |

## Exempel

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

---

## Load(*Stream*) {#load}

Läser in inställningar för tabellersättning från XML-strömmen.

```csharp
public void Load(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Ingångsström. |

## Exempel

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
