---
title: "Aspose::Words::Story::get_LastParagraph méthode"
linktitle: "get_LastParagraph"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Story::get_LastParagraph méthode. Obtient le dernier paragraphe de l'histoire en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Obtient le dernier paragraphe de l'histoire.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## Exemples



Montre comment déplacer la position du curseur d'un [DocumentBuilder](../../documentbuilder/) vers un nœud spécifié.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Le constructeur de document possède un curseur, qui agit comme la partie du document
// où le constructeur ajoute de nouveaux nœuds lorsque nous utilisons ses méthodes de construction de document.
// Ce curseur fonctionne de la même manière que le curseur clignotant de Microsoft Word,
// et il se place également **toujours** **après** tout **nœud** que le constructeur vient d'insérer.
// Pour ajouter du contenu à une autre partie du document,
// nous pouvons déplacer le curseur vers un nœud différent avec la méthode "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// Le curseur est maintenant devant le nœud vers lequel nous l'avons déplacé.
// L'ajout d'un deuxième run l'insérera devant le premier run.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Déplacez le curseur à la fin du document pour continuer à ajouter du texte à la fin comme auparavant.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Voir aussi

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
