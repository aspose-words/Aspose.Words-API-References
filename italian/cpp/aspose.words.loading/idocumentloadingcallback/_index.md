---
title: "Interfaccia Aspose::Words::Loading::IDocumentLoadingCallback"
linktitle: "IDocumentLoadingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::Loading::IDocumentLoadingCallback. Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante il caricamento di un documento in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Implementa questa interfaccia se desideri avere un tuo metodo personalizzato chiamato durante il caricamento di un documento.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | Viene chiamato per notificare l'avanzamento del caricamento del documento. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
