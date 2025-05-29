---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.FontConfigSubstitutionRule per una gestione e personalizzazione fluide dei font nei tuoi documenti. Migliora lo stile del tuo testo oggi stesso!
type: docs
weight: 3300
url: /it/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

Regola di sostituzione della configurazione del font.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | Specifica se la regola è abilitata o meno. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | Controlla se l'utilità fontconfig è disponibile o meno. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | Reimposta la cache dei risultati della chiamata fontconfig. |

## Osservazioni

Questa regola utilizza l'utilità fontconfig su Linux (e altre piattaforme simili a Unix) per ottenere la sostituzione se il font originale non è disponibile.

Se l'utilità fontconfig non è disponibile, questa regola verrà ignorata.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
