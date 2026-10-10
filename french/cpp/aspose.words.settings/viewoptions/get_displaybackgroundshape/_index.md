---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method"
linktitle: "get_DisplayBackgroundShape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method. Contrôle l'affichage de la forme d'arrière-plan dans la vue mise en page d'impression en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Contrôle l'affichage de la forme d'arrière-plan en mode mise en page d'impression.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Exemples



Montre comment masquer/afficher les images d'arrière-plan du document dans les options d'affichage.
```cpp
// Utilisez une chaîne HTML pour créer un nouveau document avec une couleur d'arrière-plan unie.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// La source du document possède un arrière-plan de couleur unie,
// dont la présence définira le drapeau "DisplayBackgroundShape" sur "true".
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Conservez le "DisplayBackgroundShape" à "true" pour que le document affiche la couleur d'arrière-plan.
// Cela peut affecter certaines couleurs de texte afin d'améliorer la visibilité.
// Définissez le "DisplayBackgroundShape" sur "false" pour ne pas afficher la couleur d'arrière-plan.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## Voir aussi

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
