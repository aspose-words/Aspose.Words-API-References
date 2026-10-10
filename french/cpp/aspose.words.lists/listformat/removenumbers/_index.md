---
title: "Aspose::Words::Lists::ListFormat::RemoveNumbers méthode"
linktitle: "RemoveNumbers"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::ListFormat::RemoveNumbers méthode. Supprime les numéros ou les puces du paragraphe actuel et définit le niveau de la liste à zéro en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.lists/listformat/removenumbers/
---
## ListFormat::RemoveNumbers method


Supprime les numéros ou puces du paragraphe actuel et définit le niveau de liste à zéro.

```cpp
void Aspose::Words::Lists::ListFormat::RemoveNumbers()
```

## Remarques


Appeler cette méthode est équivalent à définir la propriété [List](../get_list/) sur **null**.

## Exemples



Montre comment créer des listes à puces et numérotées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Ci-dessous se trouvent deux types de listes que nous pouvons créer avec un constructeur de document.
// 1 -  Une liste à puces :
// Cette liste appliquera une indentation et un symbole de puce ("•") avant chaque paragraphe.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Terminez la liste à puces.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder->get_ListFormat()->ApplyNumberDefault();

// Ce paragraphe est le premier élément. Le premier élément d’une liste numérotée aura un « 1. » comme symbole d’élément de liste.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Appelez la méthode "ListIndent" pour augmenter le niveau de liste actuel,
// ce qui démarrera une nouvelle liste autonome, avec un retrait plus important, à l'élément actuel du premier niveau de liste.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Voici les trois premiers éléments de liste du deuxième niveau, qui maintiendront une numérotation
// indépendamment de la numérotation du premier niveau de liste. Selon le format de liste actuel,
// ils auront les symboles "a.", "b.", et "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Appelez la méthode "ListOutdent" pour revenir au niveau de liste précédent.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Ces deux paragraphes continueront la numérotation du premier niveau de liste.
// Ces éléments auront les symboles "2.", et "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Si nous augmentons le niveau de liste à un niveau auquel nous avons déjà ajouté des éléments,
// la liste imbriquée sera distincte de la précédente, et sa numérotation recommencera depuis le début.
// Ces éléments de liste auront les symboles "a.", "b.", "c.", "d.", et "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Réduisez à nouveau le niveau de liste.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Terminez la liste numérotée.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


Montre comment supprimer le formatage de liste de tous les paragraphes du texte principal d'une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);
ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(paras))
{
    paragraph->get_ListFormat()->RemoveNumbers();
}

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## Voir aussi

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
