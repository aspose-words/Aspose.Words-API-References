---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::Odso class. Specifica le impostazioni dell'Office Data Source Object (ODSO) per una fonte dati di stampa unione. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.settings/odso/
---
## Odso class


Specifica le impostazioni dell'Office Data Source Object (ODSO) per una fonte dati di unione di posta. Per saperne di più, visita l'articolo di documentazione [Unione di posta e reportistica](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class Odso : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Restituisce una copia profonda di questo oggetto. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Specifica il carattere che deve essere interpretato come delimitatore di colonna usato per separare le colonne nelle fonti dati esterne. Il valore predefinito è 0, il che significa che non è definito alcun delimitatore di colonna. |
| [get_DataSource](./get_datasource/)() const | Specifica la posizione della fonte dati esterna da collegare a un documento per eseguire la stampa unione. Il valore predefinito è una stringa vuota. |
| [get_DataSourceType](./get_datasourcetype/)() const | Specifica il tipo della fonte dati esterna da collegare come parte delle informazioni di connessione ODSO per questa stampa unione. Il valore predefinito è [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Ottiene una raccolta di oggetti che specificano come le colonne della fonte dati esterna siano mappate ai nomi dei campi di stampa unione predefiniti nel documento. Questo oggetto non è mai **null**. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Specifica che un'applicazione host deve trattare la prima riga di dati nella fonte dati esterna specificata come riga di intestazione contenente i nomi di ciascuna colonna nella fonte dati. Il valore predefinito è **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Ottiene una raccolta di oggetti che specificano l'inclusione/esclusione di record individuali nella stampa unione. Questo oggetto non è mai **null**. |
| [get_TableName](./get_tablename/)() const | Specifica il particolare insieme di dati a cui una fonte deve essere collegata all'interno di una fonte dati esterna. Il valore predefinito è una stringa vuota. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per connettersi a una fonte dati esterna. Il valore predefinito è una stringa vuota. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Impostatore per [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Specifica la posizione della fonte dati esterna da collegare a un documento per eseguire la stampa unione. Il valore predefinito è una stringa vuota. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Impostatore per [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Imposta una raccolta di oggetti che specificano come le colonne della fonte dati esterna vengano mappate ai nomi dei campi di unione predefiniti nel documento. Questo oggetto non è mai **null**. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Impostatore per [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Imposta una raccolta di oggetti che specificano l'inclusione/esclusione dei singoli record nella stampa unione. Questo oggetto non è mai **null**. |
| [set_TableName](./set_tablename/)(const System::String\&) | Specifica il particolare insieme di dati a cui una fonte deve essere collegata all'interno di una fonte dati esterna. Il valore predefinito è una stringa vuota. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per connettersi a una fonte dati esterna. Il valore predefinito è una stringa vuota. |
| static [Type](./type/)() |  |
## Note


ODSO sembra essere il modo \"nuovo\" che le versioni più recenti di Microsoft Word preferiscono utilizzare quando si specificano determinati tipi di fonti dati per un documento di stampa unione. ODSO è probabilmente comparso per la prima volta in Microsoft Word 2000.

L'uso di ODSO è poco documentato e il modo migliore per imparare a utilizzare le proprietà di questo oggetto è creare manualmente in Microsoft Word un documento con la fonte dati desiderata, quindi aprire quel documento usando Aspose.Words ed esaminare le proprietà degli oggetti [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) e [Odso](../mailmergesettings/get_odso/). Questo è un buon approccio da adottare se, ad esempio, vuoi imparare come configurare programmaticamente una fonte dati.

Normalmente non è necessario creare oggetti di questa classe direttamente perché le impostazioni ODSO sono sempre disponibili tramite la proprietà [Odso](../mailmergesettings/get_odso/).

## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
