---
title: "Interfaccia Aspose::Words::Saving::IDocumentPartSavingCallback"
linktitle: "IDocumentPartSavingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::Saving::IDocumentPartSavingCallback. Implementa questa interfaccia se desideri ricevere notifiche e controllare come Aspose.Words salva le parti del documento quando esporti un documento nei formati Html o Epub in C++."
type: docs
weight: 40000
url: /it/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Implementa questa interfaccia se desideri ricevere notifiche e controllare come Aspose.Words salva le parti del documento quando esporti un documento nei formati [Html](../../aspose.words/saveformat/) o [Epub](../../aspose.words/saveformat/).

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Viene chiamata quando Aspose.Words sta per salvare una parte del documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
