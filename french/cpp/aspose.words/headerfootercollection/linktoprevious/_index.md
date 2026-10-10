---
title: "Méthode Aspose::Words::HeaderFooterCollection::LinkToPrevious"
linktitle: "LinkToPrevious"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::HeaderFooterCollection::LinkToPrevious. Lie ou détache l’en-tête ou le pied de page spécifié au (ou du) en-tête ou pied de page correspondant dans la section précédente en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/headerfootercollection/linktoprevious/
---
## HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType, bool) method


Lie ou délie l'en-tête ou le pied de page spécifié à l'en-tête ou au pied de page correspondant de la section précédente.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType headerFooterType, bool isLinkToPrevious)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Une valeur [HeaderFooterType](../../headerfootertype/) qui spécifie l’en-tête ou le pied de page à lier/détacher. |
| isLinkToPrevious | bool | **true** pour lier l’en-tête ou le pied de page à la section précédente; **false** pour détacher. |
## Remarques


Si l’en-tête ou le pied de page du type spécifié n’existe pas, il est créé automatiquement.

## Exemples



Montre comment lier les en-têtes et pieds de page entre les sections.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Déplacez-vous vers la première section et créez un en-tête et un pied de page. Par défaut,
// l’en-tête et le pied de page n’apparaîtront que sur les pages de la section qui les contient.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Nous pouvons lier les en-têtes/pieds de page d’une section à ceux de la section précédente
// pour permettre à la section de liaison d’afficher les en-têtes/pieds de page de la section liée.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Chaque section conservera ses propres objets d’en-tête/pied de page. Lorsque nous lions les sections,
// la section de liaison affichera les en-têtes/pieds de page de la section liée tout en conservant les siens.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Liez les en-têtes/pieds de page de la troisième section à ceux de la deuxième section.
// La deuxième section lie déjà les en-têtes/pieds de page de la première section,
// ainsi, lier à la deuxième section créera une chaîne de liens.
// Les première, deuxième et maintenant troisième sections afficheront toutes les en-têtes de la première section.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Nous pouvons détacher les en-têtes/pieds de page d’une section précédente en passant "false" lors de l’appel de la méthode LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Nous pouvons également sélectionner uniquement un type spécifique d’en-tête/pied de page à lier en utilisant cette méthode.
// La troisième section aura maintenant le même pied de page que les sections deuxième et première, mais pas le même en-tête.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Les en-têtes/pieds de page de la première section ne peuvent pas se lier à quoi que ce soit car il n’y a pas de section précédente.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Tous les en-têtes/pieds de page de la deuxième section sont liés aux en-têtes/pieds de page de la première section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Dans la troisième section, seul le pied de page est lié au pied de page de la première section via la deuxième section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Voir aussi

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::LinkToPrevious(bool) method


Lie ou délie tous les en-têtes et pieds de page aux en-têtes et pieds de page correspondants de la section précédente.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(bool isLinkToPrevious)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| isLinkToPrevious | bool | **true** pour lier les en-têtes et pieds de page à la section précédente ; **false** pour les délier. |
## Remarques


Si l'un des en-têtes ou pieds de page n'existe pas, il est créé automatiquement.

## Exemples



Montre comment lier les en-têtes et pieds de page entre les sections.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Déplacez-vous vers la première section et créez un en-tête et un pied de page. Par défaut,
// l’en-tête et le pied de page n’apparaîtront que sur les pages de la section qui les contient.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Nous pouvons lier les en-têtes/pieds de page d’une section à ceux de la section précédente
// pour permettre à la section de liaison d’afficher les en-têtes/pieds de page de la section liée.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Chaque section conservera ses propres objets d’en-tête/pied de page. Lorsque nous lions les sections,
// la section de liaison affichera les en-têtes/pieds de page de la section liée tout en conservant les siens.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Liez les en-têtes/pieds de page de la troisième section à ceux de la deuxième section.
// La deuxième section lie déjà les en-têtes/pieds de page de la première section,
// ainsi, lier à la deuxième section créera une chaîne de liens.
// Les première, deuxième et maintenant troisième sections afficheront toutes les en-têtes de la première section.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Nous pouvons détacher les en-têtes/pieds de page d’une section précédente en passant "false" lors de l’appel de la méthode LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Nous pouvons également sélectionner uniquement un type spécifique d’en-tête/pied de page à lier en utilisant cette méthode.
// La troisième section aura maintenant le même pied de page que les sections deuxième et première, mais pas le même en-tête.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Les en-têtes/pieds de page de la première section ne peuvent pas se lier à quoi que ce soit car il n’y a pas de section précédente.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Tous les en-têtes/pieds de page de la deuxième section sont liés aux en-têtes/pieds de page de la première section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Dans la troisième section, seul le pied de page est lié au pied de page de la première section via la deuxième section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Voir aussi

* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
