---
title: FontSubstitutionSettings Class
linktitle: FontSubstitutionSettings
articleTitle: FontSubstitutionSettings
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Fonts.FontSubstitutionSettings per una gestione efficiente dei font. Ottimizza il rendering dei documenti con opzioni di sostituzione font personalizzabili.
type: docs
weight: 3440
url: /it/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Specifica le impostazioni del meccanismo di sostituzione dei font.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FontSubstitutionSettings
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Impostazioni relative alla regola di sostituzione del font predefinito. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Impostazioni relative alla regola di sostituzione della configurazione del font. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Impostazioni relative alla regola di sostituzione delle informazioni sui font. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Impostazioni relative alla regola di sostituzione del nome del font. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Impostazioni relative alla regola di sostituzione della tabella. |

## Osservazioni

Il processo di sostituzione del font è costituito da diverse regole che vengono controllate una alla volta in un ordine specifico. Se la prima regola non riesce a risolvere il font, viene controllata la seconda regola e così via.

L'ordine delle regole è il seguente: 1. Regola di sostituzione del nome del font (abilitata per impostazione predefinita) 2. Regola di sostituzione della configurazione del font (disabilitata per impostazione predefinita) 3. Regola di sostituzione della tabella (abilitata per impostazione predefinita) 4. Regola di sostituzione delle informazioni sul font (abilitata per impostazione predefinita) 5. Regola del font predefinito (abilitata per impostazione predefinita)

Nota che la regola di sostituzione delle informazioni sul font risolverà sempre il font se[`FontInfo`](../fontinfo/) è disponibile e sovrascriverà la regola predefinita per il font. Se si desidera utilizzare la regola predefinita per il font, è necessario disabilitare la regola di sostituzione delle informazioni sul font .

Nota che la regola di sostituzione della configurazione del font risolverà il problema del font nella maggior parte dei casi e quindi sovrascriverà tutte le altre regole.

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
