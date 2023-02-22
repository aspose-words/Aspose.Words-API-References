---
title: FontConfigSubstitutionRule.Enabled
second_title: Aspose.Words per .NET API Reference
description: FontConfigSubstitutionRule proprietà. Specifica se la regola è abilitata o meno.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontconfigsubstitutionrule/enabled/
---
## FontConfigSubstitutionRule.Enabled property

Specifica se la regola è abilitata o meno.

```csharp
public override bool Enabled { set; }
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
// Su Windows, non è disponibile.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Su Linux/Mac, avremo accesso ad esso e saremo in grado di eseguire operazioni.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Guarda anche

* class [FontConfigSubstitutionRule](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontconfigsubstitutionrule/)
* assemblea [Aspose.Words](../../../)


