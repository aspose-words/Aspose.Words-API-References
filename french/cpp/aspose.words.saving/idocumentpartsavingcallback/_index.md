---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback interface"
linktitle: "IDocumentPartSavingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::IDocumentPartSavingCallback interface. Implémentez cette interface si vous souhaitez recevoir des notifications et contrôler la façon dont Aspose.Words enregistre les parties du document lors de l'exportation d'un document au format Html ou Epub en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Implémentez cette interface si vous souhaitez recevoir des notifications et contrôler la façon dont Aspose.Words enregistre les parties du document lors de l'exportation d'un document au format [Html](../../aspose.words/saveformat/) ou [Epub](../../aspose.words/saveformat/).

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Appelé lorsque Aspose.Words est sur le point d'enregistrer une partie du document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
