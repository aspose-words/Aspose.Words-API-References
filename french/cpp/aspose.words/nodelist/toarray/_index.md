---
title: "Méthode Aspose::Words::NodeList::ToArray"
linktitle: "ToArray"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::NodeList::ToArray. Copie tous les nœuds de la collection dans un nouveau tableau de nœuds en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Copie tous les nœuds de la collection dans un nouveau tableau de nœuds.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

Un tableau de nœuds.
## Remarques


Vous ne devez pas ajouter/supprimer de nœuds pendant l'itération sur une collection de nœuds car cela invalide l'itérateur et nécessite des rafraîchissements pour les collections en direct.

Pour pouvoir ajouter/supprimer des nœuds pendant l'itération, utilisez cette méthode pour copier les nœuds dans un tableau à taille fixe, puis itérez sur le tableau.

## Voir aussi

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
