---
title: "Interface Aspose::Words::Saving::IImageSavingCallback"
linktitle: "IImageSavingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::Saving::IImageSavingCallback. Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre les images lors de la sauvegarde d'un document en HTML. Peut être utilisée par d'autres formats en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre les images lors de l'enregistrement d'un document en HTML. Peut être utilisé par d'autres formats.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Appelé lorsque Aspose.Words enregistre une image en HTML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
