---
title: "Aspose::Words::IHyphenationCallback interface"
linktitle: "IHyphenationCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::IHyphenationCallback interface. Implémentée par des classes qui peuvent enregistrer des dictionnaires de césure en C++."
type: docs
weight: 78000
url: /fr/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Implémenté par des classes qui peuvent enregistrer des dictionnaires de césure.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Informe l'application que le dictionnaire de césure pour la langue spécifiée n'a pas été trouvé et qu'il peut devoir être enregistré. L'implémentation doit trouver un dictionnaire et l'enregistrer en utilisant les méthodes [RegisterDictionary()](../). Si le dictionnaire n'est pas disponible pour la langue spécifiée, l'implémentation peut se désinscrire des appels ultérieurs pour la même langue en utilisant [RegisterDictionary()](../) avec la valeur **null**. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
