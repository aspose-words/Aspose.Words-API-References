---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond méthode"
linktitle: "Respond"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond méthode. Lorsqu'elle est implémentée, renvoie une réponse de l'utilisateur lors de l'invite. Votre implémentation doit renvoyer null pour indiquer que l'utilisateur n'a pas répondu à l'invite (c'est‑à‑d. que l'utilisateur a appuyé sur le bouton Annuler dans la fenêtre d'invite) en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


Lorsqu'il est implémenté, renvoie une réponse de l'utilisateur lors de l'invite. Votre implémentation doit renvoyer **null** pour indiquer que l'utilisateur n'a pas répondu à l'invite (c'est‑à‑dire que l'utilisateur a appuyé sur le bouton Annuler dans la fenêtre d'invite).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| promptText | System::String | Texte d'invite (c.-à-d. titre de la fenêtre d'invite). |
| defaultResponse | System::String | Réponse utilisateur par défaut (c.-à-d. valeur initiale contenue dans la fenêtre d'invite). |

### ReturnValue

Réponse de l'utilisateur (c.-à-d. valeur confirmée contenue dans la fenêtre d'invite).

## Voir aussi

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
