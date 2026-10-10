---
title: "Aspose::Words::Loading::IResourceLoadingCallback interface"
linktitle: "IResourceLoadingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::IResourceLoadingCallback interface. Implementa questa interfaccia se desideri controllare come Aspose.Words carica risorse esterne durante l'importazione di un documento e l'inserimento di immagini usando DocumentBuilder in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Implementa questa interfaccia se desideri controllare come Aspose.Words carica risorse esterne durante l'importazione di un documento e l'inserimento di immagini usando [DocumentBuilder](../../aspose.words/documentbuilder/).

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Chiamata quando Aspose.Words carica qualsiasi risorsa esterna. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
