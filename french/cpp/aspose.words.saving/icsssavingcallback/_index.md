---
title: "Interface Aspose::Words::Saving::ICssSavingCallback"
linktitle: "ICssSavingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::Saving::ICssSavingCallback. Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre le CSS (Cascading Style Sheet) lors de l'enregistrement d'un document au format HTML en C++."
type: docs
weight: 39000
url: /fr/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre le CSS (Cascading [Style](../../aspose.words/style/) Sheet) lors de l'enregistrement d'un document au format HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Appelé lorsque Aspose.Words enregistre une CSS (feuille de style en cascade [Style](../../aspose.words/style/)). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
