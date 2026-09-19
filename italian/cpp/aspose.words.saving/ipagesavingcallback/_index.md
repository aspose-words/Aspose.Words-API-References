---
title: "interfaccia Aspose::Words::Saving::IPageSavingCallback"
linktitle: "IPageSavingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "interfaccia Aspose::Words::Saving::IPageSavingCallback. Implementa questa interfaccia se desideri controllare come Aspose.Words salva pagine separate quando si salva un documento in formati a pagina fissa in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


Implementa questa interfaccia se desideri controllare come Aspose.Words salva le pagine separate quando si salva un documento in formati a pagina fissa.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | Chiamata quando Aspose.Words salva una pagina separata in formati a pagina fissa. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
