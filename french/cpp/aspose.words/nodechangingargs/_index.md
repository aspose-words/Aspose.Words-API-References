---
title: "Classe Aspose::Words::NodeChangingArgs"
linktitle: "NodeChangingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::NodeChangingArgs. Fournit des données pour les méthodes de l'interface INodeChangingCallback. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words/nodechangingargs/
---
## NodeChangingArgs class


Fournit des données pour les méthodes de l'interface [INodeChangingCallback](../inodechangingcallback/). Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeChangingArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Action](./get_action/)() const | Obtient une valeur indiquant le type d'événement de changement de nœud qui se produit. |
| [get_NewParent](./get_newparent/)() const | Obtient le parent du nœud qui sera défini après la fin de l'opération. |
| [get_Node](./get_node/)() const | Obtient le [Node](./get_node/) qui est ajouté ou supprimé. |
| [get_OldParent](./get_oldparent/)() const | Obtient le parent du nœud avant le début de l'opération. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
