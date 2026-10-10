---
title: "Méthode Aspose::Words::NodeList::idx_get"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::NodeList::idx_get. Récupère un nœud à l'index donné en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Récupère un nœud à l'index donné.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un index dans la liste des nœuds. |
## Remarques


L'index commence à zéro.

Les index négatifs sont autorisés et indiquent un accès depuis la fin de la collection. Par exemple, -1 signifie le dernier élément, -2 le deuxième avant le dernier, etc.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

## Voir aussi

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
