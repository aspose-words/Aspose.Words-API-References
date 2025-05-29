---
title: FontConfigSubstitutionRule.IsFontConfigAvailable
linktitle: IsFontConfigAvailable
articleTitle: IsFontConfigAvailable
second_title: Aspose.Words per .NET
description: Scopri se l'utilità FontConfig è disponibile con il metodo IsFontConfigAvailable. Garantisci una gestione ottimale dei font per le tue applicazioni.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/
---
## FontConfigSubstitutionRule.IsFontConfigAvailable method

Controlla se l'utilità fontconfig è disponibile o meno.

```csharp
public bool IsFontConfigAvailable()
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

* class [FontConfigSubstitutionRule](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
