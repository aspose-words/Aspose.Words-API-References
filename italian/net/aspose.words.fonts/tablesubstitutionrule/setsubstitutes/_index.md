---
title: SetSubstitutes
second_title: Aspose.Words per .NET API Reference
description: Sostituisci i nomi dei font sostitutivi per il nome del font originale specificato.
type: docs
weight: 80
url: /it/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Sostituisci i nomi dei font sostitutivi per il nome del font originale specificato.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| originalFontName | String | Nome del carattere originale. |
| substituteFontNames | String[] | Elenco di nomi di caratteri alternativi. |

### Esempi

Mostra come impostare le regole di sostituzione dei caratteri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Le origini dei caratteri predefinite contengono il primo carattere utilizzato dal documento.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Il secondo font, "Amethysta", non è disponibile.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Possiamo configurare una tabella di sostituzione dei caratteri che determina
// quali caratteri Aspose.Words utilizzerà come sostituti dei caratteri non disponibili.
// Imposta due caratteri sostitutivi per "Amethysta": "Arvo" e "Courier New".
// Se il primo sostituto non è disponibile, Aspose.Words tenta di utilizzare il secondo sostituto e così via.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" non è disponibile e la regola di sostituzione afferma che il primo font da utilizzare come sostituto è "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // Anche "Arvo" non è disponibile, ma "Courier New" lo è.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Il documento di output visualizzerà il testo che utilizza il carattere "Amethysta" formattato con "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
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
