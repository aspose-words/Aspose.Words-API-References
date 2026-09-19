---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::IResourceSavingCallback interface. Implementa questa interfaccia se desideri controllare come Aspose.Words salva le risorse esterne (immagini, font e css) durante il salvataggio di un documento in HTML a pagina fissa o SVG in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Implementa questa interfaccia se desideri controllare come Aspose.Words salva le risorse esterne (immagini, font e css) quando si salva un documento in HTML a pagina fissa o SVG.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Chiamata quando Aspose.Words salva una risorsa esterna nei formati HTML a pagina fissa o SVG. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
