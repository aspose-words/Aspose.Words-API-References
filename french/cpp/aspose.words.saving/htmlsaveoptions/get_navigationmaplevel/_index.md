---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel"
linktitle: "get_NavigationMapLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel. Spécifie le niveau maximal de titres remplis dans la carte de navigation lors de l'exportation aux formats EPUB, MOBI ou AZW3. La valeur par défaut est %3 en C++."
type: docs
weight: 40500
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


Spécifie le niveau maximal de titres remplis dans la carte de navigation lors de l’exportation aux formats EPUB, MOBI ou AZW3. La valeur par défaut est **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Remarques


La carte de navigation permet aux agents utilisateurs de fournir un moyen simple de navigation à travers la structure du document. Généralement, les points de navigation correspondent aux titres du document. Afin de remplir les titres jusqu'au niveau **N**, attribuez cette valeur à [NavigationMapLevel](./).

Par défaut, trois niveaux de titres sont remplis : les paragraphes des styles **Heading 1**, **Heading 2** et **Heading 3**. Vous pouvez définir cette propriété à une valeur de 1 à 9 afin de demander le niveau maximal correspondant. La définir à zéro réduira la carte de navigation à la racine du document ou aux racines des parties du document.

## Exemples



Montre comment générer une table des matières pour les documents Azw3.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


Montre comment générer une table des matières pour les documents Mobi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
