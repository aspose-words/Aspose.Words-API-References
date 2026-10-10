---
title: "Aspose::Words::MailMerging::MailMerge::Execute metodo"
linktitle: "Esegui"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::MailMerge::Execute metodo. Esegue un'operazione di mail merge per un singolo record in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Esegue un'operazione di unione della posta per un singolo record.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Array di nomi di campi di merge. I nomi dei campi non sono sensibili al maiuscolo/minuscolo. Se viene incontrato un nome di campo che non è presente nel documento, viene ignorato. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | Array di valori da inserire nei campi di merge. Il numero di elementi in questo array deve essere lo stesso del numero di elementi in *fieldNames*. |
## Note


Usa questo metodo per riempire i campi di mail merge nel documento con valori provenienti da un array di oggetti.

Questo metodo unisce i dati per un solo record. L'array di nomi dei campi e l'array di valori rappresentano i dati di un singolo record.

Questo metodo non utilizza le regioni di mail merge.

Questo metodo ignora l'opzione [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Esempi



Mostra come unire un'immagine da un URI come dati di mail merge in un MERGEFIELD.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// I MERGEFIELD con tag "Image:" riceveranno un'immagine durante un mail merge.
// La stringa dopo i due punti nel tag "Image:" corrisponde a un nome di colonna
// nella fonte dati i cui celle contengono URI di file immagine.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Crea una fonte dati che contiene gli URI delle immagini che verranno unite.
// Un URI può essere un URL web che punta a un'immagine, oppure un nome file del file system locale di un file immagine.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Esegui una mail merge su una fonte dati con una riga.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## Vedi anche

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Esegue un'unione della posta da una fonte dati personalizzata.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Un oggetto che implementa l'interfaccia personalizzata della fonte dati per la mail merge. |
## Note


Utilizza questo metodo per riempire i campi della mail merge nel documento con valori provenienti da qualsiasi fonte dati, come una lista, una tabella hash o oggetti. È necessario scrivere la propria classe che implementa l'interfaccia [IMailMergeDataSource](../../imailmergedatasource/).

Puoi utilizzare questo metodo solo quando [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) è **false**, cioè non hai bisogno della compatibilità con le lingue da destra a sinistra (come arabo o ebraico).

Questo metodo ignora l'opzione [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Vedi anche

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
