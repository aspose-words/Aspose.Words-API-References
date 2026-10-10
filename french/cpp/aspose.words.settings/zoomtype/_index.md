---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::ZoomType enum. Valeurs possibles indiquant la taille à laquelle le document apparaît à l'écran dans Microsoft Word en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Valeurs possibles pour la taille à laquelle le document apparaît à l'écran dans Microsoft Word.

```cpp
enum class ZoomType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Personnalisé | 0 | Le pourcentage de zoom est défini explicitement. Il n'est pas recalculé automatiquement lorsque la taille du contrôle change. |
| None | n/a | Indique d'utiliser le pourcentage de zoom explicite. Identique à [Custom](./). |
| FullPage | 1 | Le pourcentage de zoom est recalculé automatiquement pour s'adapter à une page complète. |
| PageWidth | 2 | Le pourcentage de zoom est recalculé automatiquement pour s'adapter à la largeur de la page. |
| TextFit | 3 | Le pourcentage de zoom est recalculé automatiquement pour s'adapter au texte. |


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

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
