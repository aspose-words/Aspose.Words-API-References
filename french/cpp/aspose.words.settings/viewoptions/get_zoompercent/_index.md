---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method"
linktitle: "get_ZoomPercent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method. Obtient ou définit le pourcentage auquel vous souhaitez visualiser votre document en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


Obtient ou définit le pourcentage auquel vous souhaitez afficher votre document.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
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

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
