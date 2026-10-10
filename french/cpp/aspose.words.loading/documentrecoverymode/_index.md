---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::DocumentRecoveryMode enum. Spécifie les options de récupération disponibles lorsqu'un document rencontre des erreurs lors du chargement en C++."
type: docs
weight: 13500
url: /fr/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Spécifie les options de récupération disponibles lorsqu'un document rencontre des erreurs lors du chargement.

```cpp
enum class DocumentRecoveryMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucune récupération n'est tentée. Si le document est invalide, le chargement échouera avec une erreur. |
| TryRecover | 1 | Tente de récupérer le document tout en préservant le plus de données possible. |


## Exemples



Montre comment essayer de récupérer un document si des erreurs sont survenues lors du chargement.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
