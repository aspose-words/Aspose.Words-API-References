---
title: "Aspose::Words::MailMerging::FieldMergingArgs class"
linktitle: "FieldMergingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::FieldMergingArgs class. Fornisce dati per l'evento MergeField. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


Fornisce dati per l'evento **MergeField**. Per saperne di più, visita l'articolo di documentazione [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Restituisce l'oggetto [Document](../fieldmergingargsbase/get_document/) per il quale viene eseguita l'unione di posta. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Ottiene il nome del campo di unione come specificato nel documento. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Ottiene l'oggetto che rappresenta il campo di unione corrente. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Ottiene il nome del campo di unione nella fonte dati. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Ottiene il valore del campo dalla fonte dati. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Ottiene l'indice basato su zero del record che viene unito. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Ottiene il nome della tabella dati per l'operazione di unione corrente o una stringa vuota se il nome non è disponibile. |
| [get_Text](./get_text/)() const | Ottiene o imposta il testo che sarà inserito nel documento per il campo di unione corrente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Imposta il valore del campo dalla fonte dati. |
| [set_Text](./set_text/)(const System::String\&) | Setter per [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## Note


L'evento **MergeField** si verifica durante l'unione di posta quando nel documento viene incontrato un semplice campo di unione. Puoi rispondere a questo evento per restituire testo che il motore di unione di posta inserirà nel documento.

## Vedi anche

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
