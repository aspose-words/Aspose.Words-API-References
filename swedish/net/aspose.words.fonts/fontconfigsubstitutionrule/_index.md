---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FontConfigSubstitutionRule för sömlös typsnittshantering och anpassning i dina dokument. Förbättra din textstil idag!
type: docs
weight: 3300
url: /sv/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

Regel för ersättning av teckensnittskonfiguration.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | Anger om regeln är aktiverad eller inte. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | Kontrollera om fontconfig-verktyget är tillgängligt eller inte. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | Återställer cachen för fontconfig-anropsresultat. |

## Anmärkningar

Den här regeln använder verktyget fontconfig på Linux (och andra Unix-liknande) plattformar för att hämta substitutionen om det ursprungliga teckensnittet inte är tillgängligt.

Om fontconfig-verktyget inte är tillgängligt kommer den här regeln att ignoreras.

## Exempel

Visar operativsystemberoende teckensnittskonfigurationsersättning.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// FontConfigSubstitutionRule-objektet fungerar olika på Windows- och icke-Windows-plattformar.
// På Windows är den inte tillgänglig.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// På Linux/Mac kommer vi att ha tillgång till det och kunna utföra operationer.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Se även

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
