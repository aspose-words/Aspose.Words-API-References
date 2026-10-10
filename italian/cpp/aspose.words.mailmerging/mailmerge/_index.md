---
title: "Aspose::Words::MailMerging::MailMerge class"
linktitle: "MailMerge"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::MailMerge class. Rappresenta la funzionalità di unione della posta. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


Rappresenta la funzionalità di unione mail. Per saperne di più, visita l'articolo di documentazione [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMerge : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [DeleteFields](./deletefields/)() | Rimuove i campi relativi all'unione della posta dal documento. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Esegue un'unione della posta da una fonte dati personalizzata. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Esegue un'operazione di unione della posta per un singolo record. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Esegue un mail merge da una fonte dati personalizzata con regioni di mail merge. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | Esegue un mail merge da una fonte dati personalizzata con regioni di mail merge. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Ottiene un insieme di flag che specificano quali elementi devono essere rimossi durante l'unione posta. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e devono essere rimossi se è specificata l'opzione [RemoveEmptyParagraphs](../mailmergecleanupoptions/). |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | Si verifica durante il mail merge quando nel documento viene incontrato un campo di mail merge. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | Consente di gestire eventi particolari durante il mail merge. |
| [get_MappedDataFields](./get_mappeddatafields/)() | Restituisce una raccolta che rappresenta i campi dati mappati per l'operazione di mail merge. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Ottiene un valore che indica se tutte le regioni di unione posta del documento con il nome di una fonte dati devono essere unite durante l'esecuzione di un'unione posta con regioni contro la fonte dati o solo la prima. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Ottiene un valore che indica se i campi in tutto il documento vengono aggiornati durante l'esecuzione di un'unione posta con regioni. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Ottiene un valore che indica se i tag "mustache" non utilizzati devono essere conservati. |
| [get_RegionEndTag](./get_regionendtag/)() const | Ottiene il tag di chiusura della regione di unione posta. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Ottiene il tag di apertura della regione di unione posta. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Ottiene un valore che indica se le liste vengono riavviate in ogni sezione dopo l'esecuzione di un'unione posta. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Ottiene un valore che indica se il [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) della prima sezione del documento e le sue copie per le righe successive della fonte dati vengono mantenuti durante il mail merge o aggiornati secondo il comportamento di MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Restituisce un valore che indica se gli spazi bianchi iniziali e finali vengono rimossi dai valori di unione della posta. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Restituisce un valore che indica se i campi di unione e le regioni di unione vengono fusi indipendentemente dalla condizione del campo IF genitore. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Quando **true**, specifica che, oltre ai campi MERGEFIELD, l'unione della posta viene eseguita su altri tipi di campi e anche sui tag "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Restituisce un valore che indica se l'intero paragrafo con il campo **TableStart** o **TableEnd** o un intervallo specifico tra i campi **TableStart** e **TableEnd** deve essere incluso nella regione di unione della posta. |
| [GetFieldNames](./getfieldnames/)() | Restituisce una raccolta di nomi di campi di mail merge disponibili nel documento. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | Restituisce una raccolta di nomi di campi di mail merge disponibili nella regione. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | Restituisce una raccolta di nomi di campi di mail merge disponibili nella regione. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | Restituisce una raccolta di regioni di mail merge con il nome specificato. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | Restituisce una gerarchia completa di regioni (con campi) disponibili nel documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Imposta un insieme di flag che specificano quali elementi devono essere rimossi durante l'unione della posta. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Impostatore per [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | Si verifica durante il mail merge quando nel documento viene incontrato un campo di mail merge. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | Consente di gestire eventi particolari durante il mail merge. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Imposta un valore che indica se tutte le regioni di unione della posta del documento con il nome di una fonte dati devono essere unite durante l'esecuzione di un'unione della posta con regioni sulla fonte dati o solo la prima. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Imposta un valore che indica se i campi nell'intero documento vengono aggiornati durante l'esecuzione di un'unione della posta con regioni. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Imposta un valore che indica se i tag "mustache" inutilizzati devono essere conservati. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Imposta un tag di fine regione di unione della posta. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Imposta un tag di inizio regione di unione della posta. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Imposta un valore che indica se gli elenchi vengono riavviati in ogni sezione dopo l'esecuzione di un'unione della posta. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Imposta un valore che indica se il [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) della prima sezione del documento e le sue copie per le righe successive della fonte dati vengono mantenuti durante il mail merge o aggiornati secondo il comportamento di MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Imposta un valore che indica se gli spazi bianchi finali e iniziali vengono rimossi dai valori di unione della posta. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Imposta un valore che indica se i campi di unione e le regioni di unione vengono fusi indipendentemente dalla condizione del campo IF genitore. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Impostatore per [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Imposta un valore che indica se l'intero paragrafo con il campo **TableStart** o **TableEnd** o un intervallo specifico tra i campi **TableStart** e **TableEnd** deve essere incluso nella regione di unione della posta. |
| static [Type](./type/)() |  |
## Note


Per far funzionare l'operazione di mail merge, il documento deve contenere campi Word MERGEFIELD e, facoltativamente, campi NEXT. Durante l'operazione di mail merge, i campi di unione nel documento vengono sostituiti con i valori della tua fonte dati.

Esistono due modalità distinte per utilizzare il mail merge: con regioni di mail merge e senza.

Il mail merge più semplice è senza regioni ed è molto simile a come funziona il mail merge in Word. Usa i metodi **Execute** per unire le informazioni da una fonte dati come **DataTable**, **DataSet** o un array di oggetti nel tuo documento. L'oggetto [MailMerge](./) elabora tutti i record della fonte dati e copia e aggiunge il contenuto dell'intero documento per ogni record.

Nota che quando l'oggetto [MailMerge](./) incontra un campo NEXT, seleziona il record successivo nella fonte dati e continua l'unione senza copiare alcun contenuto.

Usa [ExecuteWithRegions()](../) e altri overload per unire le informazioni in un documento con regioni di mail merge definite. Puoi usarle come fonti dati per questa operazione.

È necessario utilizzare le regioni di mail merge se vuoi far crescere dinamicamente le parti all'interno del documento. Senza regioni di mail merge l'intero documento verrà ripetuto per ogni record della fonte dati.

## Vedi anche

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
