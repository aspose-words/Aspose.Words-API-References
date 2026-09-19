---
title: "Aspose::Words::Saving::IDocumentSavingCallback interfaccia"
linktitle: "IDocumentSavingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::IDocumentSavingCallback interfaccia. Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante il salvataggio di un documento in C++."
type: docs
weight: 41000
url: /it/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante il salvataggio di un documento.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | Questo è chiamato per notificare l'avanzamento del salvataggio del documento. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
