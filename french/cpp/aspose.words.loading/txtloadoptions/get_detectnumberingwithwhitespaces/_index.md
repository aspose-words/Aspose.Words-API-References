---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces méthode"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces méthode. Permet de spécifier comment les éléments de listes numérotées sont reconnus lorsque le document est importé depuis un format texte brut. La valeur par défaut est true en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Permet de spécifier comment les éléments de listes numérotées sont reconnus lorsque le document est importé à partir d'un format texte brut. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Remarques


Si cette option est définie sur **false**, l'algorithme de reconnaissance des listes détecte les paragraphes de listes lorsque les numéros de liste se terminent par un point, une parenthèse droite ou des symboles de puces (comme "•", "*", "-" ou "o").

Si cette option est définie sur **true**, les espaces sont également utilisés comme délimiteurs de numéros de liste : l'algorithme de reconnaissance des listes pour la numérotation de style arabe (1., 1.1.2.) utilise à la fois les espaces et le point (".") comme symboles.

## Exemples



Montre comment détecter les listes lors du chargement de documents texte brut.
```cpp
// Créez un document texte brut dans une chaîne avec quatre parties distinctes que nous pouvons interpréter comme des listes,
// avec différents délimiteurs. Lors du chargement du document texte brut dans un objet "Document",
// Aspose.Words détectera toujours les trois premières listes et ajoutera un objet "List"
// pour chacune à la propriété "Lists" du document.
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// Créez un objet "TxtLoadOptions", que nous pouvons passer au constructeur d'un document
// pour modifier la façon dont nous chargeons un document texte brut.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Définissez la propriété "DetectNumberingWithWhitespaces" sur "true" pour détecter les éléments numérotés
// avec des délimiteurs d'espaces, comme la quatrième liste de notre document, en tant que listes.
// Cela peut également détecter à tort des paragraphes qui commencent par des chiffres comme des listes.
// Définissez la propriété "DetectNumberingWithWhitespaces" sur "false"
// pour ne pas créer de listes à partir d'éléments numérotés avec des délimiteurs d'espaces.
loadOptions->set_DetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    ASSERT_EQ(4, doc->get_Lists()->get_Count());
    ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
else
{
    ASSERT_EQ(3, doc->get_Lists()->get_Count());
    ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
```

## Voir aussi

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
