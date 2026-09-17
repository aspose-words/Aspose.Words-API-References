---
title: "Classe Aspose::Words::Loading::ResourceLoadingArgs"
linktitle: "ResourceLoadingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Loading::ResourceLoadingArgs. Fournit des données pour la méthode ResourceLoading() en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Fournit des données pour la méthode [ResourceLoading()](../iresourceloadingcallback/resourceloading/).

```cpp
class ResourceLoadingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | URI d'origine de la ressource tel que spécifié dans le document importé. |
| [get_ResourceType](./get_resourcetype/)() const | Type de ressource. |
| [get_Uri](./get_uri/)() const | URI de la ressource utilisée pour le téléchargement si [ResourceLoading()](../iresourceloadingcallback/resourceloading/) renvoie [Default](../resourceloadingaction/). Initialement, elle est définie sur l'URI absolu de la ressource, mais l'utilisateur peut la redéfinir à n'importe quelle valeur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Définisseur pour [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Définit les données fournies par l'utilisateur pour la ressource qui sont utilisées si [ResourceLoading()](../iresourceloadingcallback/resourceloading/) renvoie [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
