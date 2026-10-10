---
title: "Interfaccia Aspose::Words::Saving::IImageSavingCallback"
linktitle: "IImageSavingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::Saving::IImageSavingCallback. Implementa questa interfaccia se desideri controllare come Aspose.Words salva le immagini durante il salvataggio di un documento in HTML. Può essere utilizzata da altri formati in C++."
type: docs
weight: 43000
url: /it/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Implementa questa interfaccia se desideri controllare come Aspose.Words salva le immagini quando si salva un documento in HTML. Può essere usato da altri formati.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Chiamata quando Aspose.Words salva un'immagine in HTML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
