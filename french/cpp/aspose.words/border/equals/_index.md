---
title: "Méthode Aspose::Words::Border::Equals"
linktitle: "Equals"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Border::Equals. Détermine si la bordure spécifiée est égale en valeur à la bordure actuelle en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/border/equals/
---
## Border::Equals(const System::SharedPtr\<Aspose::Words::Border\>\&) method


Détermine si la bordure spécifiée est égale en valeur à la bordure actuelle.

```cpp
bool Aspose::Words::Border::Equals(const System::SharedPtr<Aspose::Words::Border> &rhs)
```


## Exemples



Montre comment les collections de bordures peuvent partager des éléments.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Puisque nous avons utilisé la même configuration de bordure lors de la création
// de ces paragraphes, leurs collections de bordures partagent les mêmes éléments.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
System::SharedPtr<Aspose::Words::BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (auto&& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(Aspose::Words::LineStyle::DotDash);
}

// Après avoir modifié le style de ligne des bordures uniquement dans le deuxième paragraphe,
// les collections de bordures ne partagent plus les mêmes éléments.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Modifier l'apparence d'une bordure vide la rend visible.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## Voir aussi

* Class [Border](../)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Border::Equals(System::SharedPtr\<System::Object\>) method


Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

```cpp
bool Aspose::Words::Border::Equals(System::SharedPtr<System::Object> obj) override
```


## Exemples



Montre comment les collections de bordures peuvent partager des éléments.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Puisque nous avons utilisé la même configuration de bordure lors de la création
// de ces paragraphes, leurs collections de bordures partagent les mêmes éléments.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
System::SharedPtr<Aspose::Words::BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (auto&& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(Aspose::Words::LineStyle::DotDash);
}

// Après avoir modifié le style de ligne des bordures uniquement dans le deuxième paragraphe,
// les collections de bordures ne partagent plus les mêmes éléments.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Modifier l'apparence d'une bordure vide la rend visible.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## Voir aussi

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
