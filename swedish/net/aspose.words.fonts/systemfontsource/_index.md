---
title: SystemFontSource Class
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.SystemFontSource, din inkörsport till alla TrueType-teckensnitt på ditt system för sömlös dokumentskapande.
type: docs
weight: 3480
url: /sv/net/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class

Representerar alla TrueType-teckensnitt som är installerade i systemet.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class SystemFontSource : FontSourceBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [SystemFontSource](systemfontsource/#constructor)() | ktor. |
| [SystemFontSource](systemfontsource/#constructor_1)(*int*) | ktor. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returnerar teckensnittets källprioritet. |
| override [Type](../../aspose.words.fonts/systemfontsource/type/) { get; } | Returnerar typen av teckensnittskällan. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Anropas under bearbetning av teckensnittskälla när ett problem upptäcks som kan leda till förlust av formateringstillverkning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |
| static [GetSystemFontFolders](../../aspose.words.fonts/systemfontsource/getsystemfontfolders/)() | Returnerar systemfontmappar eller en tom array om mapparna inte är tillgängliga. |

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

### Se även

* class [FontSourceBase](../fontsourcebase/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
