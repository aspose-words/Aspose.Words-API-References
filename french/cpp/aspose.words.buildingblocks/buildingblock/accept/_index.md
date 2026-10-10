---
title: "Méthode Aspose::Words::BuildingBlocks::BuildingBlock::Accept"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::BuildingBlocks::BuildingBlock::Accept. Accepte un visiteur en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui parcourra les nœuds. |

### ReturnValue

Vrai si tous les nœuds ont été parcourus ; faux si [DocumentVisitor](../../../aspose.words/documentvisitor/) a interrompu l'opération avant de parcourir tous les nœuds.
## Remarques


Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur [DocumentVisitor](../../../aspose.words/documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

Appelle [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/), puis appelle [Accept()](../../../aspose.words/node/accept/) pour tous les nœuds enfants de ce bloc de construction, puis appelle [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Remarque : Un nœud de bloc de construction et ses enfants ne sont pas visités lorsque vous exécutez un Visitor sur un [Document](../../../aspose.words/document/). Si vous souhaitez exécuter un Visitor sur un bloc de construction, vous devez exécuter le visiteur sur le [GlossaryDocument](../../glossarydocument/) ou appeler [Accept()](./).

## Voir aussi

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
