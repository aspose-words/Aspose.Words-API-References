---
title: "Aspose::Words::Document::get_ViewOptions méthode"
linktitle: "get_ViewOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_ViewOptions method. Fournit des options pour contrôler la façon dont le document est affiché dans Microsoft Word en C++."
type: docs
weight: 58000
url: /fr/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Fournit des options pour contrôler la façon dont le document est affiché dans Microsoft Word.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
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

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
