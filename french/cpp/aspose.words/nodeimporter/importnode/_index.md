---
title: "Aspose::Words::NodeImporter::ImportNode méthode"
linktitle: "ImportNode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NodeImporter::ImportNode méthode. Importe un nœud d'un document à un autre en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Importe un nœud d'un document à un autre.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud à importer. |
| isImportChildren | bool | **true** pour importer tous les nœuds enfants de manière récursive ; sinon, **false**. |

### ReturnValue

Le nœud cloné et importé. Le nœud appartient au document de destination, mais n'a pas de parent.
## Remarques


L'importation d'un nœud crée une copie du nœud source appartenant au document d'importation. Le nœud retourné n'a pas de parent. Le nœud source n'est ni modifié ni supprimé du document original.

Avant qu'un nœud provenant d'un autre document puisse être inséré dans ce document, il doit être importé. Pendant l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Après que le nœud a été importé, il peut être inséré à l'endroit approprié dans le document en utilisant [InsertBefore1()</see> ou <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../).

Si le nœud source appartient déjà au document de destination, alors un clone profond du nœud source est simplement créé.

## Voir aussi

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
