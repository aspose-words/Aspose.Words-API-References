---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interface"
linktitle: "IFieldUserPromptRespondent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent interface. Représente le répondant aux invites utilisateur lors de la mise à jour du champ en C++."
type: docs
weight: 125000
url: /fr/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Représente le répondant aux invites de l'utilisateur pendant la mise à jour du champ.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | Lorsqu'il est implémenté, renvoie une réponse de l'utilisateur lors de l'invite. Votre implémentation doit renvoyer **null** pour indiquer que l'utilisateur n'a pas répondu à l'invite (c'est‑à‑dire que l'utilisateur a appuyé sur le bouton Annuler dans la fenêtre d'invite). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
