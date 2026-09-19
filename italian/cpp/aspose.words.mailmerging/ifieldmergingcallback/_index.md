---
title: "Aspose::Words::MailMerging::IFieldMergingCallback interfaccia"
linktitle: "IFieldMergingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::MailMerging::IFieldMergingCallback. Implementa questa interfaccia se desideri controllare come i dati vengono inseriti nei campi di unione durante un'operazione di unione della posta in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Implementa questa interfaccia se desideri controllare come i dati vengono inseriti nei campi di unione durante un'operazione di unione mail.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Chiamata quando il motore di unione della posta di Aspose.Words sta per inserire dati in un campo di unione nel documento. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Chiamata quando il motore di unione della posta di Aspose.Words sta per inserire un'immagine in un campo di unione. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
