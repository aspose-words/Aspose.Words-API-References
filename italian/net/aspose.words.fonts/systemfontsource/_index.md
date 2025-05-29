---
title: SystemFontSource Class
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.SystemFontSource, il tuo gateway per accedere a tutti i font TrueType presenti sul tuo sistema per una creazione di documenti senza interruzioni.
type: docs
weight: 3480
url: /it/net/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class

Rappresenta tutti i font TrueType installati nel sistema.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class SystemFontSource : FontSourceBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [SystemFontSource](systemfontsource/#constructor)() | Ctor. |
| [SystemFontSource](systemfontsource/#constructor_1)(*int*) | Ctor. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Restituisce la priorità della sorgente del font. |
| override [Type](../../aspose.words.fonts/systemfontsource/type/) { get; } | Restituisce il tipo di origine del font. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| static [GetSystemFontFolders](../../aspose.words.fonts/systemfontsource/getsystemfontfolders/)() | Restituisce le cartelle dei font di sistema o un array vuoto se le cartelle non sono accessibili. |

## Esempi

Mostra come accedere alla sorgente dei font di sistema di un documento e impostare i font sostitutivi.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Per impostazione predefinita, un documento vuoto contiene sempre una sorgente font di sistema.
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

// Imposta un font presente nella directory Fonts di Windows come sostituto di uno che non esiste.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// In alternativa, potremmo aggiungere una cartella font source in cui la cartella corrispondente contiene il font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Reimpostando le sorgenti dei font rimarranno comunque le sorgenti dei font di sistema e i nostri sostituti.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
```

### Guarda anche

* class [FontSourceBase](../fontsourcebase/)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
