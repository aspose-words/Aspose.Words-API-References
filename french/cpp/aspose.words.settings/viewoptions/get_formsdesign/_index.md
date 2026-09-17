---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign méthode"
linktitle: "get_FormsDesign"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign méthode. Spécifie si le document est en mode conception de formulaires en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Spécifie si le document est en mode conception de formulaires.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Remarques


Fonctionne actuellement uniquement pour les documents au format WordML.

## Exemples



Montre comment activer/désactiver le mode conception de formulaires.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Définissez la propriété "FormsDesign" sur "false" pour garder le mode conception de formulaires désactivé.
// Définissez la propriété "FormsDesign" sur "true" pour activer le mode conception de formulaires.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## Voir aussi

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
