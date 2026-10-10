---
title: "Méthode Aspose::Words::CompositeNode::SelectSingleNode"
linktitle: "SelectSingleNode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::CompositeNode::SelectSingleNode. Sélectionne le premier Node qui correspond à l'expression XPath en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


Sélectionne le premier [Node](../../node/) qui correspond à l'expression XPath.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| xpath | const System::String\& | L'expression XPath. |

### ReturnValue

Le premier [Node](../../node/) qui correspond à la requête XPath ou **null** si aucun nœud correspondant n'est trouvé.
## Remarques


Seules les expressions avec des noms d'éléments sont prises en charge pour le moment. Les expressions qui utilisent des noms d'attributs ne sont pas prises en charge.

## Voir aussi

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
