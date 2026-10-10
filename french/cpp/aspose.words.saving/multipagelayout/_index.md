---
title: "Aspose::Words::Saving::MultiPageLayout class"
linktitle: "MultiPageLayout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MultiPageLayout class. Définit une mise en page pour rendre plusieurs pages dans une sortie unique en C++."
type: docs
weight: 14500
url: /fr/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Définit une mise en page pour le rendu de plusieurs pages en une seule sortie.

```cpp
class MultiPageLayout : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Obtient la couleur d'arrière‑plan de la sortie. La valeur par défaut est **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Obtient la couleur de la bordure des pages. La valeur par défaut est **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Obtient la largeur de la bordure des pages. La valeur par défaut est 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Crée une mise en page dans laquelle les pages sont rendues de gauche à droite, de haut en bas, dans une grille avec le nombre de colonnes spécifié. |
| static [Horizontal](./horizontal/)(float) | Crée une mise en page dans laquelle toutes les pages spécifiées sont rendues horizontalement côte à côte, de gauche à droite, dans une sortie unique. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Définit la couleur d'arrière‑plan de la sortie. La valeur par défaut est **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Définit la couleur de la bordure des pages. La valeur par défaut est **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Définit la largeur de la bordure des pages. La valeur par défaut est 0. |
| static [SinglePage](./singlepage/)() | Crée une mise en page qui rend uniquement la première des pages spécifiées. |
| static [TiffFrames](./tiffframes/)() | Crée une mise en page où chaque page est rendue comme une trame distincte dans une image TIFF multi‑trames. Applicable uniquement aux formats d'image TIFF. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Crée une mise en page où toutes les pages spécifiées sont rendues verticalement, l’une sous l’autre, dans une sortie unique. |

## Exemples



Montre comment enregistrer le document en image JPG avec les paramètres de mise en page multi‑pages.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Configurez une mise en grille avec :
// - 3 colonnes par ligne.
// - Espacement de 10 pts entre les pages (horizontal et vertical).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Mises en page alternatives :
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Personnalisez l’arrière‑plan et la bordure.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
