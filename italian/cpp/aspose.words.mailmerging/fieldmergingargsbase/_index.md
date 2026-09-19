---
title: "Aspose::Words::MailMerging::FieldMergingArgsBase classe"
linktitle: "FieldMergingArgsBase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::FieldMergingArgsBase classe. Classe base per FieldMergingArgs e ImageFieldMergingArgs. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.mailmerging/fieldmergingargsbase/
---
## FieldMergingArgsBase class


Classe base per [FieldMergingArgs](../fieldmergingargs/) e [ImageFieldMergingArgs](../imagefieldmergingargs/). Per saperne di più, visita l'articolo di documentazione [Unione di stampa e reportistica](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgsBase : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Document](./get_document/)() const | Restituisce l'oggetto [Document](./get_document/) per il quale viene eseguito il mail merge. |
| [get_DocumentFieldName](./get_documentfieldname/)() const | Ottiene il nome del campo di unione come specificato nel documento. |
| [get_Field](./get_field/)() const | Ottiene l'oggetto che rappresenta il campo di unione corrente. |
| [get_FieldName](./get_fieldname/)() const | Ottiene il nome del campo di unione nella fonte dati. |
| [get_FieldValue](./get_fieldvalue/)() const | Ottiene il valore del campo dalla fonte dati. |
| [get_RecordIndex](./get_recordindex/)() const | Ottiene l'indice basato su zero del record che viene unito. |
| [get_TableName](./get_tablename/)() const | Ottiene il nome della tabella dati per l'operazione di unione corrente o una stringa vuota se il nome non è disponibile. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](./set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Imposta il valore del campo dalla fonte dati. |
| static [Type](./type/)() |  |

## Vedi anche

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
