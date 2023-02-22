---
title: Class FontSubstitutionSettings
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fonts.FontSubstitutionSettings classe. Specifica le impostazioni del meccanismo di sostituzione dei caratteri.
type: docs
weight: 2830
url: /it/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Specifica le impostazioni del meccanismo di sostituzione dei caratteri.

```csharp
public class FontSubstitutionSettings
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Impostazioni relative alla regola di sostituzione dei caratteri predefinita. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Impostazioni relative alla regola di sostituzione della configurazione dei caratteri. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Impostazioni relative alla regola di sostituzione delle informazioni sui caratteri. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Impostazioni relative alla regola di sostituzione del nome del carattere. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Impostazioni relative alla regola di sostituzione delle tabelle. |

### Osservazioni

Il processo di sostituzione dei caratteri consiste in diverse regole che vengono controllate una per una in un ordine specifico. Se la prima regola non riesce a risolvere il carattere, viene controllata la seconda regola e così via.

L'ordine delle regole è il seguente: 1. Regola di sostituzione del nome del carattere (attivata per impostazione predefinita) 2. Regola di sostituzione della configurazione del carattere (disattivata per impostazione predefinita) 3. Regola di sostituzione della tabella (attivata per impostazione predefinita) 4. Regola di sostituzione delle informazioni del carattere (abilitata per impostazione predefinita) 5. Regola dei caratteri predefinita (abilitata per impostazione predefinita)

Nota che la regola di sostituzione delle informazioni sul carattere risolverà sempre il carattere se[`FontInfo`](../fontinfo/) è disponibile e sovrascriverà la regola dei caratteri predefinita. Se desideri utilizzare la regola dei caratteri predefinita, devi disabilitare la regola di sostituzione delle informazioni sui caratteri .

Nota che la regola di sostituzione della configurazione del carattere risolverà il carattere nella maggior parte dei casi e quindi sovrascriverà tutte le altre regole.

### Esempi

Mostra come accedere all'origine dei caratteri di sistema di un documento e impostare i caratteri sostitutivi.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Per impostazione predefinita, un documento vuoto contiene sempre un'origine del carattere di sistema.
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

// Imposta un carattere che esiste nella directory dei caratteri di Windows come sostituto di uno che non lo è.
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

// Il ripristino delle fonti dei caratteri ci lascia ancora con la fonte dei caratteri di sistema e i nostri sostituti.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)


