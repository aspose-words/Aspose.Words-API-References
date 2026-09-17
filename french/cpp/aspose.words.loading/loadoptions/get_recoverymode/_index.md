---
title: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode méthode"
linktitle: "get_RecoveryMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode méthode. Définit comment le document doit être traité en cas d'erreurs lors du chargement. Utilisez cette propriété pour spécifier si le système doit tenter de récupérer le document ou suivre un autre comportement défini. La valeur par défaut est TryRecover en C++."
type: docs
weight: 14500
url: /fr/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


Définit comment le document doit être traité en cas d'erreurs lors du chargement. Utilisez cette propriété pour spécifier si le système doit tenter de récupérer le document ou suivre un autre comportement défini. La valeur par défaut est [TryRecover](../../documentrecoverymode/).

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## Exemples



Montre comment essayer de récupérer un document si des erreurs sont survenues lors du chargement.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Voir aussi

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
