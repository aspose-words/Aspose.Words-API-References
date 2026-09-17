---
title: "Aspose::Words::Node::get_ParentNode méthode"
linktitle: "get_ParentNode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::get_ParentNode méthode. Obtient le parent immédiat de ce nœud en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Obtient le parent immédiat de ce nœud.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Remarques


Si un nœud vient d'être créé et n'a pas encore été ajouté à l'arbre, ou s'il a été retiré de l'arbre, le parent est **null**.

## Exemples



Montre comment accéder au nœud parent d'un nœud.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Ajoutez un nœud Run enfant au premier paragraphe du document.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Le paragraphe est le nœud parent du nœud Run. Nous pouvons tracer cette lignée
// jusqu'au nœud document, qui est la racine de l'arbre de nœuds du document.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


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

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
