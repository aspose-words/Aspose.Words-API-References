---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method"
linktitle: "get_LoadFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method. Spécifie le format du document à charger. La valeur par défaut est Auto en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Spécifie le format du document à charger. La valeur par défaut est [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Remarques


Il est recommandé de spécifier la valeur [Auto](../../../aspose.words/loadformat/) et de laisser Aspose.Words détecter automatiquement le format du fichier. Si vous connaissez le format du document que vous vous apprêtez à charger, vous pouvez spécifier le format explicitement, ce qui réduira légèrement le temps de chargement en évitant le surcoût lié à la détection automatique du format. Si vous spécifiez un format de chargement explicite et qu'il s'avère incorrect, la détection automatique sera invoquée et une seconde tentative de chargement du fichier sera effectuée.

## Exemples



Montre comment spécifier une URI de base lors de l'ouverture d'un document html.
```cpp
// Supposons que nous voulions charger un document .html contenant une image liée par une URI relative
// alors que l'image se trouve à un autre emplacement. Dans ce cas, nous devrons résoudre l'URI relative en une URI absolue.
// Nous pouvons fournir une URI de base en utilisant un objet HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Bien que l'image était cassée dans le .html d'entrée, notre URI de base personnalisée nous a aidés à réparer le lien.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Ce document de sortie affichera l'image qui manquait.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Voir aussi

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
