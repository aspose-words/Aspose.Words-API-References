---
title: AddSubstitutes
second_title: Aspose.Words per .NET API Reference
description: Aggiunge i nomi dei font sostitutivi per il nome del font originale specificato.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/tablesubstitutionrule/addsubstitutes/
---
## TableSubstitutionRule.AddSubstitutes method

Aggiunge i nomi dei font sostitutivi per il nome del font originale specificato.

```csharp
public void AddSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| originalFontName | String | Nome del carattere originale. |
| substituteFontNames | String[] | Elenco di nomi di caratteri alternativi. |

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

Mostra come lavorare con le tabelle di sostituzione dei caratteri personalizzate.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Crea una nuova regola di sostituzione delle tabelle e carica la tabella di sostituzione dei caratteri predefinita di Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Se selezioniamo i caratteri esclusivamente dalla nostra cartella, avremo bisogno di una tabella di sostituzione personalizzata.
// Non avremo più accesso ai font di Microsoft Windows,
// come "Arial" o "Times New Roman" poiché non esistono nella nostra nuova cartella dei caratteri.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Di seguito sono riportati due modi per caricare una tabella di sostituzione da un file nel file system locale.
// 1 - Da un flusso:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Direttamente da un file:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Dal momento che non abbiamo più accesso ad "Arial", la nostra tabella dei caratteri proverà prima a sostituirlo con "Carattere inesistente".
// Non abbiamo questo font in modo che si sposterà sul successivo sostituto, "Kreon", che si trova nella cartella "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Possiamo espandere questa tabella a livello di codice. Aggiungeremo una voce che sostituisce "Times New Roman" con "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Possiamo aggiungere un sostituto secondario di fallback per una voce di carattere esistente con AddSubstitutes().
// Nel caso in cui "Arvo" non sia disponibile, la nostra tabella cercherà "M+ 2m" come seconda opzione sostitutiva.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() può impostare un nuovo elenco di caratteri sostitutivi per un carattere.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// La scrittura di testo in caratteri a cui non abbiamo accesso invocherà le nostre regole di sostituzione.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Guarda anche

* class [TableSubstitutionRule](../)
* spazio dei nomi [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
