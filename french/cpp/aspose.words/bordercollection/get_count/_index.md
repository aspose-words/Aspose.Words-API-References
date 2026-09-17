---
title: "Aspose::Words::BorderCollection::get_Count méthode"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection::get_Count méthode. Obtient le nombre de bordures dans la collection en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/bordercollection/get_count/
---
## BorderCollection::get_Count method


Obtient le nombre de bordures dans la collection.

```cpp
int32_t Aspose::Words::BorderCollection::get_Count()
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

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
