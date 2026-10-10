---
title: "Méthode Aspose::Words::BorderCollection::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::BorderCollection::ClearFormatting. Supprime toutes les bordures d'un objet en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Supprime toutes les bordures d'un objet.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Exemples



Montre comment supprimer toutes les bordures de tous les paragraphes d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Le premier paragraphe de ce document possède des bordures visibles avec ces paramètres.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// Utilisez la méthode "ClearFormatting" sur chaque paragraphe pour supprimer toutes les bordures.
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    paragraph->get_ParagraphFormat()->get_Borders()->ClearFormatting();

    for (auto&& border : System::IterateOver(paragraph->get_ParagraphFormat()->get_Borders()))
    {
        ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
        ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());
        ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
    }
}

doc->Save(get_ArtifactsDir() + u"BorderCollection.RemoveAllBorders.docx");
```

## Voir aussi

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
