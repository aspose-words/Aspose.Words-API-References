---
title: "Aspose::Words::MailMerging::IMailMergeDataSource interfaccia"
linktitle: "IMailMergeDataSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::IMailMergeDataSource interfaccia. Implementa questa interfaccia per consentire il mail merge da una fonte dati personalizzata, come un elenco di oggetti. I dati master-detail sono supportati anche in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Implementa questa interfaccia per consentire l'unione mail da una fonte dati personalizzata, come un elenco di oggetti. Sono supportati anche dati master-detail.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Restituisce il nome della fonte dati. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | Il motore di mail merge di Aspose.Words invoca questo metodo quando incontra l'inizio di una regione di mail merge annidata. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | Avanza al record successivo nella fonte dati. |
| static [Type](./type/)() |  |
## Note


Quando una fonte dati viene creata, dovrebbe essere inizializzata per puntare a BOF (prima del primo record). Il motore di mail merge di Aspose.Words invocherà [MoveNext](./movenext/) per avanzare al record successivo e poi invocherà [GetValue()](./getvalue/) per ogni campo di merge incontrato nel documento o nella regione di mail merge corrente.

## Vedi anche

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
