---
title: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes méthode"
linktitle: "GetChildNodes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes méthode. Retourne une collection dynamique de nœuds enfants correspondant au type spécifié en C++."
type: docs
weight: 34500
url: /fr/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


Renvoie une collection dynamique de nœuds enfants qui correspondent au type spécifié.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Spécifie le type de nœuds à sélectionner. |
| isDeep | bool | **true** pour sélectionner parmi tous les nœuds enfants de façon récursive ; **false** pour ne sélectionner que parmi les enfants immédiats. |

### ReturnValue

Une collection dynamique d'enfants du type spécifié.
## Remarques


La collection de nœuds renvoyée par cette méthode est toujours dynamique.

Une collection dynamique est toujours synchronisée avec le document. Par exemple, si vous sélectionnez toutes les sections d'un document et parcourez la collection en supprimant les sections, la section est retirée de la collection immédiatement lorsqu'elle est supprimée du document.

## Voir aussi

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
