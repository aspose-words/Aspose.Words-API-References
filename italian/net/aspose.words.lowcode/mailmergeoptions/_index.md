---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.MailMergeOptions per soluzioni di stampa unione a basso codice e senza interruzioni. Migliora l'automazione dei tuoi documenti con funzionalità personalizzabili!
type: docs
weight: 4260
url: /it/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

Rappresenta le opzioni per la funzionalità di unione di posta.

```csharp
public class MailMergeOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | Ottiene o imposta un set di flag che specificano quali elementi devono essere rimossi durante la stampa unione. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e dovrebbero essere rimossi seRemoveEmptyParagraphs l'opzione è specificata. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | Ottiene o imposta un valore che indica se tutte le aree di unione di documenti con il nome di un'origine dati devono essere unite durante l'esecuzione di un'unione di documenti con aree relative all'origine dati o solo la prima. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | Ottiene o imposta un valore che indica se i campi dell'intero documento vengono aggiornati durante l'esecuzione di una stampa unione con regioni. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | Ottiene o imposta un valore che indica se i tag "baffi" non utilizzati devono essere conservati. |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | Ottiene o imposta un tag di fine regione di unione di posta. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | Ottiene o imposta un tag di inizio regione di unione di posta. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | Ottiene o imposta un valore che indica se gli elenchi vengono riavviati a ogni sezione dopo l'esecuzione di una stampa unione. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | Ottiene o imposta un valore che indica se l'inizio della sezione della prima sezione del documento e le sue copie per le righe successive della sorgente dati vengono mantenute durante la stampa unione o aggiornate in base al comportamento di MS Word. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | Ottiene o imposta un valore che indica se gli spazi vuoti iniziali e finali vengono tagliati dai valori di unione di posta. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Ottiene o imposta un valore che indica se i campi di unione e le regioni di unione vengono uniti indipendentemente dalla condizione del campo IF padre. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | Quando`VERO` , specifica che oltre ai campi MERGEFIELD, la stampa unione viene eseguita in alcuni altri tipi di campi e anche nei tag "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Ottiene o imposta un valore che indica se l'intero paragrafo con**TableStart** O**TableEnd** field o intervallo particolare tra**TableStart** E**TableEnd** i campi dovrebbero essere inclusi nell'area di unione della stampa. |

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
