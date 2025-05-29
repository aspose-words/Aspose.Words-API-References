---
title: FontSubstitutionRule Class
linktitle: FontSubstitutionRule
articleTitle: FontSubstitutionRule
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.FontSubstitutionRule: la tua guida essenziale per una sostituzione efficace dei font nell'elaborazione e nella progettazione dei documenti.
type: docs
weight: 3430
url: /it/net/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class

Questa è una classe base astratta per la regola di sostituzione dei font.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public abstract class FontSubstitutionRule
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Specifica se la regola è abilitata o meno. |

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
