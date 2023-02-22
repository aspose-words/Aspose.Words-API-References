---
title: FontSettings.SubstitutionSettings
second_title: Aspose.Words per .NET API Reference
description: FontSettings proprietà. Impostazioni relative al meccanismo di sostituzione dei caratteri.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontsettings/substitutionsettings/
---
## FontSettings.SubstitutionSettings property

Impostazioni relative al meccanismo di sostituzione dei caratteri.

```csharp
public FontSubstitutionSettings SubstitutionSettings { get; }
```

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

* class [FontSubstitutionSettings](../../fontsubstitutionsettings/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontsettings/)
* assemblea [Aspose.Words](../../../)


