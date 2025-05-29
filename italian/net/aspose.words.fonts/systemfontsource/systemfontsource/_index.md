---
title: SystemFontSource
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: Aspose.Words per .NET
description: Scopri il costruttore SystemFontSource per una gestione efficiente dei font. Migliora il tuo web design con soluzioni tipografiche ottimizzate oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.fonts/systemfontsource/systemfontsource/
---
## SystemFontSource() {#constructor}

Ctor.

```csharp
public SystemFontSource()
```

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

* class [SystemFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## SystemFontSource(*int*) {#constructor_1}

Ctor.

```csharp
public SystemFontSource(int priority)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| priority | Int32 | Priorità della sorgente del font. Vedi[`Priority`](../../fontsourcebase/priority/) descrizione della proprietà per maggiori informazioni. |

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

* class [SystemFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
