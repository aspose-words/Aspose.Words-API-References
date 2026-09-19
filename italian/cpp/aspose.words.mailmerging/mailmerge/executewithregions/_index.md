---
title: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions metodo"
linktitle: "ExecuteWithRegions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions metodo. Esegue un'unione di stampa da una fonte dati personalizzata con regioni di unione di stampa in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Esegue un mail merge da una fonte dati personalizzata con regioni di mail merge.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Un oggetto che implementa l'interfaccia personalizzata della fonte dati per la mail merge. |
## Note


Utilizza questo metodo per compilare i campi di unione di stampa nel documento con valori provenienti da qualsiasi fonte dati personalizzata, come un file XML o collezioni di oggetti business. È necessario scrivere la propria classe che implementa l'interfaccia [IMailMergeDataSource](../../imailmergedatasource/).

Puoi utilizzare questo metodo solo quando [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) è **false**, cioè non hai bisogno della compatibilità con le lingue da destra a sinistra (come arabo o ebraico).

## Vedi anche

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Esegue un mail merge da una fonte dati personalizzata con regioni di mail merge.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | Un oggetto che implementa l'interfaccia personalizzata della radice della fonte dati di unione di stampa. |
## Note


Utilizza questo metodo per compilare i campi di unione di stampa nel documento con valori provenienti da qualsiasi fonte dati personalizzata, come un file XML o collezioni di oggetti business. È necessario scrivere le proprie classi che implementano le interfacce [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) e [IMailMergeDataSource](../../imailmergedatasource/).

Puoi utilizzare questo metodo solo quando [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) è **false**, cioè non hai bisogno della compatibilità con le lingue da destra a sinistra (come arabo o ebraico).

## Vedi anche

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
