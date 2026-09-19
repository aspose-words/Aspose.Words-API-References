---
title: "Classe Aspose::Words::LowCode::MailMergeOptions"
linktitle: "MailMergeOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::LowCode::MailMergeOptions. Rappresenta le opzioni per la funzionalità di unione posta in C++."
type: docs
weight: 750
url: /it/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


Rappresenta le opzioni per la funzionalità di stampa unione.

```cpp
class MailMergeOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Ottiene un insieme di flag che specificano quali elementi devono essere rimossi durante l'unione posta. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e devono essere rimossi se l'opzione [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/) è specificata. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Ottiene un valore che indica se tutte le regioni di unione posta del documento con il nome di una fonte dati devono essere unite durante l'esecuzione di un'unione posta con regioni contro la fonte dati o solo la prima. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Ottiene un valore che indica se i campi in tutto il documento vengono aggiornati durante l'esecuzione di un'unione posta con regioni. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Ottiene un valore che indica se i tag "mustache" non utilizzati devono essere conservati. |
| [get_RegionEndTag](./get_regionendtag/)() const | Ottiene il tag di chiusura della regione di unione posta. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Ottiene il tag di apertura della regione di unione posta. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Ottiene un valore che indica se le liste vengono riavviate in ogni sezione dopo l'esecuzione di un'unione posta. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Ottiene un valore che indica se l'inizio sezione della prima sezione del documento e le sue copie per le righe successive della fonte dati vengono mantenuti durante l'unione posta o aggiornati secondo il comportamento di MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Restituisce un valore che indica se gli spazi bianchi iniziali e finali vengono rimossi dai valori di unione della posta. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Restituisce un valore che indica se i campi di unione e le regioni di unione vengono fusi indipendentemente dalla condizione del campo IF genitore. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Quando **true**, specifica che, oltre ai campi MERGEFIELD, l'unione della posta viene eseguita su altri tipi di campi e anche sui tag "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Restituisce un valore che indica se l'intero paragrafo con il campo **TableStart** o **TableEnd** o un intervallo specifico tra i campi **TableStart** e **TableEnd** deve essere incluso nella regione di unione della posta. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Imposta un insieme di flag che specificano quali elementi devono essere rimossi durante l'unione della posta. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Metodo impostatore per [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Imposta un valore che indica se tutte le regioni di unione della posta del documento con il nome di una fonte dati devono essere unite durante l'esecuzione di un'unione della posta con regioni sulla fonte dati o solo la prima. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Imposta un valore che indica se i campi nell'intero documento vengono aggiornati durante l'esecuzione di un'unione della posta con regioni. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Imposta un valore che indica se i tag "mustache" inutilizzati devono essere conservati. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Imposta un tag di fine regione di unione della posta. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Imposta un tag di inizio regione di unione della posta. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Imposta un valore che indica se gli elenchi vengono riavviati in ogni sezione dopo l'esecuzione di un'unione della posta. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Imposta un valore che indica se l'inizio della prima sezione del documento e le sue copie per le righe successive della fonte dati vengono mantenuti durante l'unione della posta o aggiornati secondo il comportamento di MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Imposta un valore che indica se gli spazi bianchi finali e iniziali vengono rimossi dai valori di unione della posta. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Imposta un valore che indica se i campi di unione e le regioni di unione vengono fusi indipendentemente dalla condizione del campo IF genitore. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Metodo impostatore per [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Imposta un valore che indica se l'intero paragrafo con il campo **TableStart** o **TableEnd** o un intervallo specifico tra i campi **TableStart** e **TableEnd** deve essere incluso nella regione di unione della posta. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
