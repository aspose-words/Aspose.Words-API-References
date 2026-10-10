---
title: "Aspose::Words::Saving::IFontSavingCallback interface"
linktitle: "IFontSavingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::IFontSavingCallback interface. Implémentez cette interface si vous souhaitez recevoir des notifications et contrôler la façon dont Aspose.Words enregistre les polices lors de l'exportation d'un document au format HTML en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Implémentez cette interface si vous souhaitez recevoir des notifications et contrôler la façon dont Aspose.Words enregistre les polices lors de l'exportation d'un document au format HTML.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Appelé lorsque Aspose.Words est sur le point d'enregistrer une ressource de police. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
