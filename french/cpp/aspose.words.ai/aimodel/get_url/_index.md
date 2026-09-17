---
title: "Méthode Aspose::Words::AI::AiModel::get_Url"
linktitle: "get_Url"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::AI::AiModel::get_Url. Obtient ou définit l'URL du modèle. La valeur par défaut est spécifique au modèle en C++."
type: docs
weight: 2834
url: /fr/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Obtient ou définit l'URL du modèle. La valeur par défaut est spécifique au modèle.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Exemples



Montre comment modifier l'URL par défaut du modèle.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Valeur par défaut "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## Voir aussi

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
