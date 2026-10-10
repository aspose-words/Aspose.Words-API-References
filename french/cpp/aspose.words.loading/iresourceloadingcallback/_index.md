---
title: "Aspose::Words::Loading::IResourceLoadingCallback interface"
linktitle: "IResourceLoadingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::IResourceLoadingCallback interface. Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words charge les ressources externes lors de l'importation d'un document et de l'insertion d'images à l'aide de DocumentBuilder en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words charge les ressources externes lors de l'importation d'un document et de l'insertion d'images à l'aide de [DocumentBuilder](../../aspose.words/documentbuilder/).

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Appelé lorsque Aspose.Words charge une ressource externe. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
