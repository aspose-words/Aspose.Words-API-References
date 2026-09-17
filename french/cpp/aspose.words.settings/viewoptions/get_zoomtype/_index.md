---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomType method"
linktitle: "get_ZoomType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomType method. Obtient ou définit une valeur de zoom basée sur la taille de la fenêtre en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.settings/viewoptions/get_zoomtype/
---
## ViewOptions::get_ZoomType method


Obtient ou définit une valeur de zoom basée sur la taille de la fenêtre.

```cpp
Aspose::Words::Settings::ZoomType Aspose::Words::Settings::ViewOptions::get_ZoomType() const
```


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

* Enum [ZoomType](../../zoomtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
