---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::IMailMergeCallback interface. Implementa questa interfaccia se desideri ricevere notifiche durante l'esecuzione dell'unione di posta in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Implementa questa interfaccia se desideri ricevere notifiche durante l'esecuzione dell'unione mail.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Chiamato quando i tag di testo "mustache" vengono sostituiti con campi MERGEFIELD. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
