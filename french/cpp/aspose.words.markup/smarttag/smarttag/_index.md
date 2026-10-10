---
title: "Aspose::Words::Markup::SmartTag::SmartTag constructeur"
linktitle: "SmartTag"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::SmartTag::SmartTag constructeur. Initialise une nouvelle instance de la classe SmartTag en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Initialise une nouvelle instance de la classe [SmartTag](../).

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
## Remarques


Lorsque vous créez un nouveau nœud, vous devez spécifier un document auquel le nœud appartient. Un nœud ne peut pas exister sans document car il dépend des structures du document telles que les listes et les styles. Bien qu'un nœud appartienne toujours à un document, il peut ou ne peut pas faire partie de l'arborescence du document.

Lorsqu'un nœud est créé, il appartient à un document, mais n'est pas encore partie de l'arborescence du document et [ParentNode](../../../aspose.words/node/get_parentnode/) est nul. Pour insérer un nœud dans le document, utilisez les méthodes [InsertAfter1()</see> ou <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) sur le nœud parent.

## Voir aussi

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
