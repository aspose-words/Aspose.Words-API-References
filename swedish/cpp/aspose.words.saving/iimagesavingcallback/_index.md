---
title: "Aspose::Words::Saving::IImageSavingCallback interface"
linktitle: "IImageSavingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::IImageSavingCallback interface. Implementera detta gränssnitt om du vill kontrollera hur Aspose.Words sparar bilder när ett dokument sparas till HTML. Kan användas av andra format i C++."
type: docs
weight: 43000
url: /sv/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Implementera detta gränssnitt om du vill kontrollera hur Aspose.Words sparar bilder när ett dokument sparas till HTML. Kan användas av andra format.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Kallas när Aspose.Words sparar en bild till HTML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
