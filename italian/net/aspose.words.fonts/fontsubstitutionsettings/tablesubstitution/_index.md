---
title: FontSubstitutionSettings.TableSubstitution
linktitle: TableSubstitution
articleTitle: TableSubstitution
second_title: Aspose.Words per .NET
description: Esplora FontSubstitutionSettings per regole di sostituzione delle tabelle ottimali. Migliora il tuo design con impostazioni efficaci per una gestione fluida dei font.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/
---
## FontSubstitutionSettings.TableSubstitution property

Impostazioni relative alla regola di sostituzione della tabella.

```csharp
public TableSubstitutionRule TableSubstitution { get; }
```

## Esempi

Mostra come lavorare con tabelle di sostituzione dei font personalizzate.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Crea una nuova regola di sostituzione tabella e carica la tabella di sostituzione dei font predefinita di Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Se selezioniamo i font esclusivamente dalla nostra cartella, avremo bisogno di una tabella di sostituzione personalizzata.
// Non avremo più accesso ai font di Microsoft Windows,
// come "Arial" o "Times New Roman" poiché non sono presenti nella nostra nuova cartella dei font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Di seguito sono riportati due metodi per caricare una tabella di sostituzione da un file nel file system locale.
// 1 - Da un flusso:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Direttamente da un file:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Poiché non abbiamo più accesso ad "Arial", la nostra tabella dei font proverà prima a sostituirlo con "Nonexistent Font".
// Non disponiamo di questo font, quindi verrà spostato sul successivo sostituto, "Kreon", che si trova nella cartella "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Possiamo espandere questa tabella programmaticamente. Aggiungeremo una voce che sostituisce "Times New Roman" con "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Possiamo aggiungere un sostituto secondario di fallback per una voce di font esistente con AddSubstitutes().
// Nel caso in cui "Arvo" non sia disponibile, la nostra tabella cercherà "M+ 2m" come seconda opzione sostitutiva.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() può impostare un nuovo elenco di font sostitutivi per un font.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// La scrittura di testo in font a cui non abbiamo accesso invocherà le nostre regole di sostituzione.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Guarda anche

* class [TableSubstitutionRule](../../tablesubstitutionrule/)
* class [FontSubstitutionSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
