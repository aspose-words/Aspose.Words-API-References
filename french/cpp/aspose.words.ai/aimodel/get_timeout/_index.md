---
title: "Méthode Aspose::Words::AI::AiModel::get_Timeout"
linktitle: "get_Timeout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::AI::AiModel::get_Timeout. Obtient ou définit le nombre de millisecondes à attendre avant que la requête au modèle d'IA n'expire. La valeur par défaut est de 100 000 millisecondes (100 secondes) en C++."
type: docs
weight: 2667
url: /fr/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


Obtient ou définit le nombre de millisecondes à attendre avant que la requête au modèle [AI](../../) n'expire. La valeur par défaut est de 100 000 millisecondes (100 secondes).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Exemples



Montre comment modifier le délai d'expiration par défaut du modèle.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Valeur par défaut 100000 ms.
model->set_Timeout(250000);
```

## Voir aussi

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
