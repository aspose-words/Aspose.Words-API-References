---
title: "Classe Aspose::Words::Settings::ViewOptions"
linktitle: "ViewOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::ViewOptions class. Fournit diverses options qui contrôlent la façon dont un document est affiché dans Microsoft Word. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Fournit diverses options qui contrôlent la façon dont un document est affiché dans Microsoft Word. Pour en savoir plus, consultez l'article de documentation [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/).

```cpp
class ViewOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Contrôle l'affichage de la forme d'arrière-plan en mode mise en page d'impression. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Désactive l'affichage de l'espace entre le haut du texte et le bord supérieur de la page. |
| [get_FormsDesign](./get_formsdesign/)() const | Spécifie si le document est en mode conception de formulaires. |
| [get_ViewType](./get_viewtype/)() const | Contrôle le mode d'affichage dans Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | Obtient ou définit le pourcentage auquel vous souhaitez afficher votre document. |
| [get_ZoomType](./get_zoomtype/)() const | Obtient ou définit une valeur de zoom basée sur la taille de la fenêtre. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Définisseur pour [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Définisseur pour [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | Définisseur pour [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Définisseur pour [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Définisseur pour [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Définisseur pour [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment définir un facteur de zoom personnalisé, que les versions antérieures de Microsoft Word appliqueront à un document lors du chargement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


Montre comment définir un type de zoom personnalisé, que les versions plus anciennes de Microsoft Word appliqueront à un document lors du chargement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Définissez la propriété "ZoomType" sur "ZoomType.PageWidth" pour obtenir Microsoft Word
// pour zoomer automatiquement le document afin d'ajuster la largeur de la page.
// Définissez la propriété "ZoomType" sur "ZoomType.FullPage" pour obtenir Microsoft Word
// pour zoomer automatiquement le document afin de rendre toute la première page visible.
// Définissez la propriété "ZoomType" sur "ZoomType.TextFit" pour obtenir Microsoft Word
// pour zoomer automatiquement le document afin d'ajuster les marges internes du texte de la première page.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
