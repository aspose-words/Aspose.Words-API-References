---
title: FontSubstitutionSettings.FontConfigSubstitution
linktitle: FontConfigSubstitution
articleTitle: FontConfigSubstitution
second_title: Aspose.Words per .NET
description: Esplora FontSubstitutionSettings per una configurazione ottimizzata dei font. Scopri come migliorare la tipografia con efficaci regole di sostituzione per un design migliore.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

Impostazioni relative alla regola di sostituzione della configurazione del font.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

## Esempi

Mostra la sostituzione della configurazione dei font in base al sistema operativo.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// L'oggetto FontConfigSubstitutionRule funziona in modo diverso sulle piattaforme Windows e non Windows.
// Su Windows non è disponibile.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Su Linux/Mac avremo accesso ad esso e potremo eseguire operazioni.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Guarda anche

* class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
