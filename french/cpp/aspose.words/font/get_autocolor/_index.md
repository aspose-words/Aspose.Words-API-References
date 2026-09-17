---
title: "Aspose::Words::Font::get_AutoColor méthode"
linktitle: "get_AutoColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_AutoColor méthode. Retourne la couleur calculée actuelle du texte (noir ou blanc) à utiliser pour ''auto color''. Si la couleur n'est pas ''auto'', alors retourne Color en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Retourne la couleur calculée actuelle du texte (noir ou blanc) à utiliser pour 'auto color'. Si la couleur n'est pas 'auto', alors retourne [Color](../get_color/).

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Remarques


Lorsque le texte a une 'couleur automatique', la couleur réelle du texte est calculée automatiquement afin qu'elle soit lisible par rapport à la couleur de fond. Lorsque vous modifiez la couleur de fond, la couleur du texte basculera automatiquement en noir ou blanc dans MS Word pour maximiser la lisibilité.

## Exemples



Montre comment améliorer la lisibilité en sélectionnant automatiquement la couleur du texte en fonction de la luminosité de son arrière-plan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si l'objet Font d'un run ne spécifie pas de couleur de texte, il le fera automatiquement
// sélectionnera soit le noir soit le blanc en fonction de la couleur du fond.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// La couleur par défaut du texte est le noir. Si la couleur du fond est sombre, le texte noir sera difficile à voir.
// Pour résoudre ce problème, la propriété AutoColor affichera ce texte en blanc.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// Si nous changeons le fond en une couleur claire, le noir sera un peu plus
// approprié que le blanc, de sorte que la couleur automatique l'affichera en noir.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
