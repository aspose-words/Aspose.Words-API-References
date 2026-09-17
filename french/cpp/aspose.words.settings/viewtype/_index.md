---
title: "Énumération Aspose::Words::Settings::ViewType"
linktitle: "ViewType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Settings::ViewType. Valeurs possibles pour le mode d’affichage dans Microsoft Word en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Valeurs possibles pour le mode d'affichage dans Microsoft Word.

```cpp
enum class ViewType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Le document sera rendu dans la vue par défaut de l’application. |
| Lecture | 0 | Le document sera rendu dans la vue par défaut de l’application. |
| MiseEnPage | 1 | Le document sera ouvert dans une vue qui affiche le document tel qu’il sera imprimé. |
| Outline | 3 | Le document sera rendu dans une vue optimisée pour le plan ou la création de longs documents. |
| Normal | 4 | Le document sera rendu dans une vue optimisée pour le plan ou la création de longs documents. |
| Web | 5 | Le document sera rendu dans une vue imitant la façon dont ce document serait affiché dans une page web. |


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
