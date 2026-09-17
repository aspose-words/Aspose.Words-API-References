---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::IResourceSavingCallback interface. Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre les ressources externes (images, polices et css) lors de l'enregistrement d'un document au format HTML ou SVG à pages fixes en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre les ressources externes (images, polices et css) lors de l'enregistrement d'un document en HTML ou SVG à page fixe.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Appelé lorsque Aspose.Words enregistre une ressource externe aux formats HTML ou SVG à pages fixes. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
