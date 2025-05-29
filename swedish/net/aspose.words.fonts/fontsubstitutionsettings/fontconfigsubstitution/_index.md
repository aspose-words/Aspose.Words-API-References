---
title: FontSubstitutionSettings.FontConfigSubstitution
linktitle: FontConfigSubstitution
articleTitle: FontConfigSubstitution
second_title: Aspose.Words för .NET
description: Utforska FontSubstitutionSettings för optimerad typsnittskonfiguration. Upptäck hur du kan förbättra typografi med effektiva ersättningsregler för bättre design.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

Inställningar relaterade till ersättningsregel för teckensnittskonfiguration.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

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

* class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
