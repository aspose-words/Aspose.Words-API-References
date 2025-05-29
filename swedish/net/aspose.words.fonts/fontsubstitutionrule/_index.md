---
title: FontSubstitutionRule Class
linktitle: FontSubstitutionRule
articleTitle: FontSubstitutionRule
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FontSubstitutionRule – din viktiga guide för effektiv typsnittsersättning i dokumentbehandling och design.
type: docs
weight: 3430
url: /sv/net/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class

Detta är en abstrakt basklass för teckensnittsersättningsregeln.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public abstract class FontSubstitutionRule
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Anger om regeln är aktiverad eller inte. |

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

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
