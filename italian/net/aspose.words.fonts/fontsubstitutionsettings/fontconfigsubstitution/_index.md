---
title: FontSubstitutionSettings.FontConfigSubstitution
second_title: Aspose.Words per .NET API Reference
description: FontSubstitutionSettings proprietà. Impostazioni relative alla regola di sostituzione della configurazione dei caratteri.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

Impostazioni relative alla regola di sostituzione della configurazione dei caratteri.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

### Esempi

Mostra la sostituzione della configurazione dei caratteri dipendente dal sistema operativo.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// L'oggetto FontConfigSubstitutionRule funziona in modo diverso su piattaforme Windows/non Windows.
// Su Windows non è disponibile.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Su Linux/Mac avremo accesso ad esso e saremo in grado di eseguire operazioni.
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
* spazio dei nomi [Aspose.Words.Fonts](../../fontsubstitutionsettings/)
* assemblea [Aspose.Words](../../../)


