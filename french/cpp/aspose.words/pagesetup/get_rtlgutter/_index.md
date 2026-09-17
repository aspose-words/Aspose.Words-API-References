---
title: "Aspose::Words::PageSetup::get_RtlGutter method"
linktitle: "get_RtlGutter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_RtlGutter method. Obtient ou définit si Microsoft Word utilise des gouttières pour la section en fonction d’une langue de droite à gauche ou d’une langue de gauche à droite en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Obtient ou définit si Microsoft Word utilise des gouttières pour la section en fonction d’une langue de droite à gauche ou de gauche à droite.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
```


## Exemples



Montre comment définir les marges de gouttière.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez du texte qui s’étend sur plusieurs pages.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Une gouttière ajoute des espaces blancs à la marge gauche ou droite de la page,
// ce qui compense le pliage central des pages d’un livre empiétant sur la mise en page de la page.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Déterminez l’espace disponible pour le texte à l’intérieur des marges de nos pages, puis ajoutez une valeur pour élargir une marge.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Définissez la propriété "RtlGutter" sur "true" pour placer la gouttière à une position plus adaptée au texte de droite à gauche.
pageSetup->set_RtlGutter(true);

// Définissez la propriété "MultiplePages" sur "MultiplePagesType.MirrorMargins" pour alterner
// la position des marges côté gauche/droite à chaque page.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
