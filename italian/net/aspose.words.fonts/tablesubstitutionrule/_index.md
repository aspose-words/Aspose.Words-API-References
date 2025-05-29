---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
articleTitle: TableSubstitutionRule
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.TableSubstitutionRule per una gestione efficiente dei font e una formattazione del testo impeccabile nei tuoi documenti.
type: docs
weight: 3490
url: /it/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Regola di sostituzione dei caratteri della tabella.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Specifica se la regola è abilitata o meno. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(*string, params string[]*) | Aggiunge nomi di font sostitutivi per il nome del font originale specificato. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(*string*) | Restituisce un array contenente i nomi dei font sostitutivi per il nome del font originale specificato. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(*Stream*) | Carica le impostazioni di sostituzione della tabella dal flusso XML. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(*string*) | Carica le impostazioni di sostituzione della tabella dal file XML. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Carica le impostazioni predefinite di sostituzione delle tabelle per la piattaforma Android. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Carica le impostazioni predefinite di sostituzione delle tabelle per la piattaforma Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Carica le impostazioni predefinite di sostituzione delle tabelle per la piattaforma Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(*Stream*) | Salva le impostazioni di sostituzione della tabella corrente nel flusso. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(*string*) | Salva le impostazioni di sostituzione della tabella corrente nel file. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(*string, params string[]*) | Sostituisce i nomi dei font sostitutivi con il nome del font originale fornito. |

## Osservazioni

Questa regola definisce l'elenco dei nomi di font sostitutivi da utilizzare se il font originale non è disponibile. I sostituti verranno controllati per il nome del font e il[`AltName`](../fontinfo/altname/) (se presente).

## Esempi

Mostra come accedere alle tabelle di sostituzione dei font per Windows e Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Crea una nuova regola di sostituzione tabella e carica la tabella di sostituzione font predefinita di Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// In Windows, il sostituto predefinito del font "Times New Roman CE" è "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Possiamo salvare la tabella sotto forma di documento XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux ha la sua tabella di sostituzione.
// Esistono diversi font sostitutivi per "Times New Roman CE".
// Se anche il primo sostituto, "FreeSerif", non è disponibile,
// questa regola scorrerà le altre nell'array finché non ne troverà una disponibile.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Salva la tabella di sostituzione di Linux sotto forma di documento XML utilizzando un flusso.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Guarda anche

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
