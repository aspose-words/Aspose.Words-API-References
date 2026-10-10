---
title: "Aspose::Words::EditorType enum"
linktitle: "EditorType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::EditorType enum. Spécifie l'ensemble des alias possibles (ou groupes d'édition) qui peuvent être utilisés comme alias pour déterminer si l'utilisateur actuel doit être autorisé à modifier une plage unique définie par une plage modifiable dans un document en C++."
type: docs
weight: 88000
url: /fr/cpp/aspose.words/editortype/
---
## EditorType enum


Spécifie l'ensemble des alias possibles (ou groupes d'édition) qui peuvent être utilisés comme alias pour déterminer si l'utilisateur actuel est autorisé à modifier une plage unique définie par une plage modifiable dans un document.

```cpp
enum class EditorType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Non spécifié | 0 | Indique que le type d'éditeur n'est pas spécifié. |
| Administrateurs | 1 | Spécifie que les utilisateurs associés au groupe Administrateurs sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| Contributeurs | 2 | Spécifie que les utilisateurs associés au groupe Contributeurs sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| Actuel | 3 | Spécifie que les utilisateurs associés au groupe Actuel sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| Éditeurs | 4 | Spécifie que les utilisateurs associés au groupe Éditeurs sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| Tous | 5 | Spécifie que tous les utilisateurs qui ouvrent le document sont autorisés à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| None | 6 | Spécifie qu'aucun des utilisateurs qui ouvrent le document n'est autorisé à modifier les plages modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| Propriétaires | 7 | Spécifie que les utilisateurs associés au groupe Propriétaires sont autorisés à modifier les zones modifiables en utilisant ce type d'édition lorsque la protection du document est activée. |
| Default | n/a | Identique à [Non spécifié](./). |

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
