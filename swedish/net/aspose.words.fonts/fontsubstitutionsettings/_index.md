---
title: FontSubstitutionSettings Class
linktitle: FontSubstitutionSettings
articleTitle: FontSubstitutionSettings
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fonts.FontSubstitutionSettings för effektiv typsnittshantering. Optimera dokumentrendering med anpassningsbara alternativ för typsnittsersättning.
type: docs
weight: 3440
url: /sv/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Anger inställningar för mekanismen för teckensnittsersättning.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FontSubstitutionSettings
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Inställningar relaterade till standardregeln för teckensnittsersättning. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Inställningar relaterade till ersättningsregel för teckensnittskonfiguration. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Inställningar relaterade till regel för ersättning av teckensnittsinformation. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Inställningar relaterade till regel för ersättning av teckensnittsnamn. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Inställningar relaterade till tabellersättningsregel. |

## Anmärkningar

Teckensnittsersättningsprocessen består av flera regler som kontrolleras en efter en i specifik ordning. Om den första regeln inte kan matcha teckensnittet kontrolleras den andra regeln och så vidare.

Reglernas ordning är följande: 1. Regel för ersättning av teckensnittsnamn (aktiverad som standard) 2. Regel för ersättning av teckensnittskonfiguration (inaktiverad som standard) 3. Regel för ersättning av tabell (aktiverad som standard) 4. Regel för ersättning av teckensnittsinformation (aktiverad som standard) 5. Standardregel för teckensnitt (aktiverad som standard)

Observera att regeln för ersättning av teckensnittsinformation alltid löser teckensnittet om[`FontInfo`](../fontinfo/) är tillgänglig och kommer att åsidosätta standardteckensnittsregeln. Om du vill använda standardteckensnittsregeln bör du inaktivera ersättningsregeln för teckensnittsinformation .

Observera att ersättningsregeln för teckensnitt i de flesta fall löser teckensnittet och därmed åsidosätter alla andra regler.

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

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
