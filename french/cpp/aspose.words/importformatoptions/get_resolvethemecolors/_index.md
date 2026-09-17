---
title: "Méthode Aspose::Words::ImportFormatOptions::get_ResolveThemeColors"
linktitle: "get_ResolveThemeColors"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ImportFormatOptions::get_ResolveThemeColors. Obtient ou définit une valeur booléenne qui indique s’il faut résoudre les couleurs de thème des formes de manière forcée. La valeur par défaut est false en C++."
type: docs
weight: 8500
url: /fr/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Obtient ou définit une valeur booléenne qui indique s'il faut résoudre de manière forcée les couleurs de thème des formes. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Remarques


Veuillez noter que cette option n’est pertinente que pour le mode [KeepSourceFormatting](../../importformatmode/).

Normalement, Aspose.Words ne résout pas les couleurs de thème source lors de l’importation lorsque les styles peuvent être conservés sans développer les attributs de formatage en attributs directs. Cependant, dans ce cas, les couleurs réelles des formes importées peuvent différer de celles qu’elles avaient dans le document original. La raison en est les différentes couleurs de thème dans les documents source et de destination. Activer cette option en la réglant sur **true** force la résolution des couleurs de thème des formes source et permet ainsi de conserver la couleur réelle des formes présentes dans le document source.

## Exemples



Montre comment importer un nœud en résolvant les couleurs de thème source des formes.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Déplacez-vous vers le pied de page principal et insérez une forme qui utilise les couleurs du thème.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importez le pied de page source dans le document de destination avec les couleurs du thème résolues,
// afin que la forme conserve sa couleur réelle du document source.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
