---
title: "Méthode Aspose::Words::IHyphenationCallback::RequestDictionary. Notifie l'application que le dictionnaire de césure pour la langue spécifiée n'a pas été trouvé et peut devoir être enregistré. L'implémentation doit trouver un dictionnaire et l'enregistrer en utilisant les méthodes RegisterDictionary(). Si le dictionnaire n'est pas disponible pour la langue spécifiée, l'implémentation peut se désinscrire des appels ultérieurs pour la même langue en utilisant RegisterDictionary() avec une valeur null en C++."
linktitle: "Méthode Aspose::Words::IHyphenationCallback::GetType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Comment utiliser la méthode GetType de la classe Aspose::Words::IHyphenationCallback en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Informe l'application que le dictionnaire de césure pour la langue spécifiée n'a pas été trouvé et qu'il peut devoir être enregistré. L'implémentation doit trouver un dictionnaire et l'enregistrer en utilisant les méthodes [RegisterDictionary()](../). Si le dictionnaire n'est pas disponible pour la langue spécifiée, l'implémentation peut se désinscrire des appels ultérieurs pour la même langue en utilisant [RegisterDictionary()](../) avec la valeur **null**.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| langue | System::String | Un nom de langue, par ex. "en-US". Voir la documentation .NET pour "culture name" et le RFC 4646 pour plus de détails. |

## Voir aussi

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
