---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept méthode"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept méthode. Accepte un visiteur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui parcourra les nœuds. |

### ReturnValue

Vrai si tous les nœuds ont été parcourus ; faux si [DocumentVisitor](../../../aspose.words/documentvisitor/) a interrompu l'opération avant de parcourir tous les nœuds.
## Remarques


Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur [DocumentVisitor](../../../aspose.words/documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

Appelle [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/), puis appelle [Accept()](../../../aspose.words/node/accept/) pour tous les nœuds enfants de ce nœud et enfin appelle [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) à la fin.

Remarque : Un nœud de document glossary et ses enfants ne sont pas visités lorsque vous exécutez un Visitor sur un [Document](../../../aspose.words/document/). Si vous souhaitez exécuter un Visitor sur un document glossary, vous devez appeler [Accept()](./).

## Voir aussi

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
