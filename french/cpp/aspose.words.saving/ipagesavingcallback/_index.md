---
title: "interface Aspose::Words::Saving::IPageSavingCallback"
linktitle: "IPageSavingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "interface Aspose::Words::Saving::IPageSavingCallback. Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre des pages séparées lors de l'enregistrement d'un document aux formats de pages fixes en C++."
type: docs
weight: 44000
url: /fr/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre les pages séparées lors de l'enregistrement d'un document dans des formats de page fixe.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | Appelé lorsque Aspose.Words enregistre une page séparée aux formats de pages fixes. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
