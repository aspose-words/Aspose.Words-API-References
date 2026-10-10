---
title: "Aspose::Words::Node::get_Document méthode"
linktitle: "get_Document"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::get_Document méthode. Obtient le document auquel ce nœud appartient en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/node/get_document/
---
## Node::get_Document method


Obtient le document auquel ce nœud appartient.

```cpp
virtual System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Node::get_Document() const
```

## Remarques


Le nœud appartient toujours à un document même s'il vient d'être créé et n'a pas encore été ajouté à l'arbre, ou s'il a été retiré de l'arbre.

## Exemples



Montre comment créer un nœud et définir son document propriétaire.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Nous n'avons pas encore ajouté ce paragraphe en tant qu'enfant à aucun nœud composite.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// Si un nœud est d'un type d'enfant approprié pour un autre nœud composite,
// nous pouvons le rattacher en tant qu'enfant uniquement si les deux nœuds ont le même document propriétaire.
// Le document propriétaire est le document que nous avons passé au constructeur du nœud.
// Nous n'avons pas attaché ce paragraphe au document, donc le document ne contient pas son texte.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// Puisque le document possède ce paragraphe, nous pouvons appliquer l'un de ses styles au contenu du paragraphe.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Ajoutez ce nœud au document, puis vérifiez son contenu.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Voir aussi

* Class [DocumentBase](../../documentbase/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
