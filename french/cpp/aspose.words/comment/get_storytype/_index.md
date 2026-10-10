---
title: "Aspose::Words::Comment::get_StoryType méthode"
linktitle: "get_StoryType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comment::get_StoryType méthode. Retourne les Commentaires en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/comment/get_storytype/
---
## Comment::get_StoryType method


Retourne [Comments](../../storytype/).

```cpp
Aspose::Words::StoryType Aspose::Words::Comment::get_StoryType() override
```


## Exemples



Montre comment insérer des nœuds [InlineStory](../../inlinestory/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// Les nœuds de tableau ont une méthode "EnsureMinimum()" qui garantit que le tableau possède au moins une cellule.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// Nous pouvons placer un tableau à l'intérieur d'une note de bas de page, ce qui le fera apparaître dans le pied de page de la page de référence.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// Un InlineStory possède également une méthode "EnsureMinimum()", mais dans ce cas,
// cela garantit que le dernier enfant du nœud est un paragraphe,
// pour que nous puissions cliquer et écrire du texte facilement dans Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Modifiez l'apparence de l'ancre, qui est le petit chiffre en exposant
// dans le texte principal qui pointe vers la note de bas de page.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// Tous les nœuds d'histoire en ligne ont leurs types d'histoire respectifs.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// Un commentaire est un autre type d'histoire en ligne.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// Le paragraphe parent d'un nœud d'histoire en ligne sera celui du corps principal du document.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// Cependant, le dernier paragraphe est celui du contenu texte du commentaire,
// qui sera en dehors du corps principal du document dans une bulle de texte.
// Un commentaire n'aura aucun nœud enfant par défaut,
// ainsi nous pouvons appliquer la méthode EnsureMinimum() pour placer également un paragraphe ici.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Une fois que nous avons un paragraphe, nous pouvons déplacer le constructeur pour le faire et écrire notre commentaire.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## Voir aussi

* Enum [StoryType](../../storytype/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
