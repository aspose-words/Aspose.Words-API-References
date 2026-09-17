---
title: "Aspose::Words::Border::ClearFormatting méthode"
linktitle: "ClearFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Border::ClearFormatting méthode. Réinitialise les propriétés de bordure aux valeurs par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/border/clearformatting/
---
## Border::ClearFormatting method


Réinitialise les propriétés de la bordure aux valeurs par défaut.

```cpp
void Aspose::Words::Border::ClearFormatting()
```


## Exemples



Montre comment supprimer les bordures d'un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Chaque paragraphe possède un ensemble individuel de bordures.
// Nous pouvons accéder aux paramètres d'apparence de ces bordures via l'objet de format de paragraphe.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// Nous pouvons supprimer une bordure en une fois en exécutant la méthode ClearFormatting.
// L'exécution de cette méthode sur chaque bordure d'un paragraphe supprimera toutes ses bordures.
for (auto&& border : System::IterateOver(borders))
{
    border->ClearFormatting();
}

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, borders->idx_get(0)->get_LineStyle());
ASSERT_FALSE(borders->idx_get(0)->get_IsVisible());

doc->Save(get_ArtifactsDir() + u"Border.ClearFormatting.docx");
```

## Voir aussi

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
