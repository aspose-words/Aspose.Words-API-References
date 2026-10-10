---
title: "Aspose::Words::Settings::ViewOptions::get_ViewType méthode"
linktitle: "get_ViewType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::ViewOptions::get_ViewType méthode. Contrôle le mode d'affichage dans Microsoft Word en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.settings/viewoptions/get_viewtype/
---
## ViewOptions::get_ViewType method


Contrôle le mode d'affichage dans Microsoft Word.

```cpp
Aspose::Words::Settings::ViewType Aspose::Words::Settings::ViewOptions::get_ViewType() const
```

## Remarques


Bien qu'Aspose.Words puisse lire et écrire cette option, son utilisation est spécifique à l'application. Par exemple, MS Word 2013 ne respecte pas la valeur de cette option.

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

* Enum [ViewType](../../viewtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
