---
title: Class TableSubstitutionRule
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fonts.TableSubstitutionRule classe. Regola di sostituzione dei caratteri della tabella.
type: docs
weight: 3060
url: /it/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Regola di sostituzione dei caratteri della tabella.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

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
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(string, params string[]) | Aggiunge nomi di font sostitutivi per il nome del font originale specificato. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(string) | Restituisce l'array contenente i nomi dei font sostitutivi per il nome del font originale specificato. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(Stream) | Carica le impostazioni di sostituzione della tabella dal flusso XML. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(string) | Carica le impostazioni di sostituzione della tabella dal file XML. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Carica le impostazioni di sostituzione della tabella predefinite per la piattaforma Android. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Carica le impostazioni di sostituzione della tabella predefinite per la piattaforma Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Carica le impostazioni di sostituzione della tabella predefinite per la piattaforma Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(Stream) | Salva le impostazioni di sostituzione della tabella correnti nello streaming. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(string) | Salva le impostazioni di sostituzione della tabella correnti nel file. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(string, params string[]) | Sostituisci i nomi dei caratteri sostitutivi per il nome del carattere originale specificato. |

### Osservazioni

Questa regola definisce l'elenco dei nomi dei font sostitutivi da utilizzare se il font originale non è disponibile. Verranno controllati i sostituti per il nome del font e il[`AltName`](../fontinfo/altname/) (se presente).

### Esempi

Mostra come accedere alle tabelle di sostituzione dei caratteri per Windows e Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Crea una nuova regola di sostituzione della tabella e carica la tabella di sostituzione dei caratteri predefinita di Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// In Windows, il sostituto predefinito del carattere "Times New Roman CE" è "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Possiamo salvare la tabella sotto forma di documento XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux ha la propria tabella di sostituzione.
// Esistono più caratteri sostitutivi per "Times New Roman CE".
// Se anche il primo sostituto, "FreeSerif", non è disponibile,
// questa regola scorrerà le altre nell'array finché non ne troverà una disponibile.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Salva la tabella di sostituzione Linux sotto forma di documento XML utilizzando uno stream.
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


