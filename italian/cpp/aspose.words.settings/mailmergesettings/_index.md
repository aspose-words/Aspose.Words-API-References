---
title: "classe Aspose::Words::Settings::MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Settings::MailMergeSettings. Specifica tutte le informazioni di stampa unione per un documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


Specifica tutte le informazioni di unione di posta per un documento. Per saperne di più, visita l'articolo di documentazione [Unione di posta e reportistica](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMergeSettings : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clear](./clear/)() | Cancella le impostazioni di stampa unione in modo che, quando il documento viene salvato, nessuna impostazione di stampa unione venga salvata e il documento diventi normale. |
| [Clone](./clone/)() | Restituisce una copia profonda di questo oggetto. |
| [get_ActiveRecord](./get_activerecord/)() const | Specifica l'indice basato su 1 del record della fonte dati che deve essere visualizzato in Microsoft Word. Il valore predefinito è 1. |
| [get_AddressFieldName](./get_addressfieldname/)() const | Specifica la colonna nella fonte dati che contiene gli indirizzi e-mail. Il valore predefinito è una stringa vuota. |
| [get_CheckErrors](./get_checkerrors/)() const | Specifica il tipo di segnalazione degli errori che Microsoft Word deve eseguire durante una stampa unione. Il valore predefinito è [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | Specifica la stringa di connessione utilizzata per collegarsi a una fonte dati esterna. Il valore predefinito è una stringa vuota. |
| [get_DataSource](./get_datasource/)() const | Specifica il percorso della fonte dati di stampa unione. Il valore predefinito è una stringa vuota. |
| [get_DataType](./get_datatype/)() const | Specifica il tipo della fonte dati di stampa unione e il metodo di accesso ai dati. Il valore predefinito è [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | Specifica come Microsoft Word produrrà i risultati di una stampa unione. Il valore predefinito è [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. Il valore predefinito è **false**. |
| [get_HeaderSource](./get_headersource/)() const | Specifica il percorso della sorgente dell'intestazione di stampa unione. Il valore predefinito è una stringa vuota. |
| [get_LinkToQuery](./get_linktoquery/)() const | Non sono sicuro di questo. La Microsoft Word Automation Reference suggerisce che questo specifichi che la query viene eseguita ogni volta che il documento viene aperto in Microsoft Word. Ma la specifica OOXML suggerisce che questo specifichi che la query contiene un riferimento a un file di query esterno che contiene la query effettiva. Il valore predefinito è **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati via e-mail come allegato anziché nel corpo dell'e-mail reale. Il valore predefinito è **false**. |
| [get_MailSubject](./get_mailsubject/)() const | Specifica il testo che deve apparire nella riga dell'oggetto delle e-mail o fax prodotti durante la stampa unione. Il valore predefinito è una stringa vuota. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | Specifica il tipo di documento principale della stampa unione. Il valore predefinito è [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | Ottiene l'oggetto che specifica le impostazioni dell'Office Data Source Object (ODSO). |
| [get_Query](./get_query/)() const | Contiene la stringa Structured Query Language che deve essere eseguita contro la fonte dati esterna specificata per restituire l'insieme di record da importare nel documento quando viene eseguita l'operazione di stampa unione. Il valore predefinito è una stringa vuota. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | Specifica che Microsoft Word deve visualizzare i dati dalla fonte dati esterna specificata dove sono stati inseriti i campi di stampa unione (ad esempio anteprima dei dati uniti). Il valore predefinito è **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | Specifica l'indice basato su 1 del record della fonte dati che deve essere visualizzato in Microsoft Word. Il valore predefinito è 1. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | Specifica la colonna nella fonte dati che contiene gli indirizzi e-mail. Il valore predefinito è una stringa vuota. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | Specifica il tipo di segnalazione degli errori che Microsoft Word deve eseguire durante una stampa unione. Il valore predefinito è [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | Specifica la stringa di connessione utilizzata per collegarsi a una fonte dati esterna. Il valore predefinito è una stringa vuota. |
| [set_DataSource](./set_datasource/)(const System::String\&) | Specifica il percorso della fonte dati di stampa unione. Il valore predefinito è una stringa vuota. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | Specifica il tipo della fonte dati di stampa unione e il metodo di accesso ai dati. Il valore predefinito è [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | Specifica come Microsoft Word produrrà i risultati di una stampa unione. Il valore predefinito è [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. Il valore predefinito è **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | Specifica il percorso della sorgente dell'intestazione di stampa unione. Il valore predefinito è una stringa vuota. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | Setter per [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/). |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati via e-mail come allegato anziché nel corpo dell'e-mail reale. Il valore predefinito è **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | Specifica il testo che deve apparire nella riga dell'oggetto delle e-mail o fax prodotti durante la stampa unione. Il valore predefinito è una stringa vuota. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | Setter per [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/). |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | Imposta l'oggetto che specifica le impostazioni dell'Office Data Source Object (ODSO). |
| [set_Query](./set_query/)(const System::String\&) | Contiene la stringa Structured Query Language che deve essere eseguita contro la fonte dati esterna specificata per restituire l'insieme di record da importare nel documento quando viene eseguita l'operazione di stampa unione. Il valore predefinito è una stringa vuota. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | Specifica che Microsoft Word deve visualizzare i dati dalla fonte dati esterna specificata dove sono stati inseriti i campi di stampa unione (ad esempio anteprima dei dati uniti). Il valore predefinito è **false**. |
| static [Type](./type/)() |  |
## Note


Puoi usare questo oggetto per specificare una fonte dati di stampa unione per un documento e queste informazioni (insieme ai campi dati disponibili) appariranno in Microsoft Word quando l'utente apre il documento. Oppure puoi usare questo oggetto per interrogare le impostazioni di stampa unione che l'utente ha specificato in Microsoft Word per questo documento.

Normalmente non è necessario creare oggetti di questa classe direttamente perché le impostazioni di stampa unione di un documento sono sempre disponibili tramite la proprietà [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/).

Per rilevare se questo documento è il documento principale di un'unione di stampa, controlla il valore della proprietà [MainDocumentType](./get_maindocumenttype/).

Per rimuovere le impostazioni di unione di stampa e le informazioni sulla fonte dati da un documento puoi utilizzare il metodo [Clear](./clear/). Aspose.Words non scriverà le impostazioni di unione di stampa in un documento se la proprietà [MainDocumentType](./get_maindocumenttype/) è impostata su [NotAMergeDocument](../mailmergemaindocumenttype/) o la proprietà [DataType](./get_datatype/) è impostata su [None](../mailmergedatatype/).

Il modo migliore per imparare a utilizzare le proprietà di questo oggetto è creare manualmente in Microsoft Word un documento con la fonte dati desiderata, quindi aprire quel documento con Aspose.Words ed esaminare le proprietà degli oggetti [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) e [Odso](./get_odso/). Questo è un buon approccio da adottare se, ad esempio, vuoi imparare a configurare programmaticamente una fonte dati.

Aspose.Words conserva le informazioni di unione di stampa durante il caricamento, il salvataggio e la conversione dei documenti tra diversi formati, ma non utilizza queste informazioni quando esegue la propria unione di stampa usando l'oggetto [MailMerge](../../aspose.words.mailmerging/mailmerge/).

## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
