---
title: "Méthode Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd"
linktitle: "VisitGlossaryDocumentEnd"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd. Appelée lorsque l'énumération d'un document de glossaire s'est terminée en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor::VisitGlossaryDocumentEnd method


Appelé lorsque l'énumération d'un document de glossaire est terminée.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| glossaire | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | L'objet qui est visité. |

### ReturnValue

Une valeur [VisitorAction](../../visitoraction/) qui spécifie comment poursuivre l'énumération.
## Remarques


Remarque : Un nœud de document de glossaire et ses enfants ne sont pas parcourus lorsque vous exécutez un Visitor sur un [Document](../../document/). Si vous souhaitez exécuter un Visitor sur un document de glossaire, vous devez appeler [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/).

## Voir aussi

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
