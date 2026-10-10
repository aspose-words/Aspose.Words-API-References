---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance méthode"
linktitle: "get_DefaultInstance"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance méthode. Paramètres de police par défaut statiques en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Paramètres de police par défaut statiques.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Exemples



Montre comment configurer l'instance des paramètres de police par défaut.
```cpp
// Configurez l'instance des paramètres de police par défaut pour utiliser la police "Courier New"
// comme substitut de secours lorsque nous essayons d'utiliser une police inconnue.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// Ce document n'a pas de configuration FontSettings. Lors du rendu du document,
// l'instance par défaut de FontSettings résoudra la police manquante.
// Aspose.Words utilisera "Courier New" pour rendre le texte qui utilise la police inconnue.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## Voir aussi

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
