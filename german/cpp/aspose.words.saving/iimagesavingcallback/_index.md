---
title: "Aspose::Words::Saving::IImageSavingCallback Schnittstelle"
linktitle: "IImageSavingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::IImageSavingCallback Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words Bilder beim Speichern eines Dokuments nach HTML speichert. Kann von anderen Formaten in C++ verwendet werden."
type: docs
weight: 43000
url: /de/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie Aspose.Words Bilder beim Speichern eines Dokuments nach HTML speichert. Kann von anderen Formaten verwendet werden.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Wird aufgerufen, wenn Aspose.Words ein Bild nach HTML speichert. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
