---
title: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode"
linktitle: "get_ListExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode. Spécifie comment les éléments de liste seront écrits dans le fichier de sortie. La valeur par défaut est MarkdownSyntax en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Spécifie comment les éléments de liste seront écrits dans le fichier de sortie. La valeur par défaut est [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Remarques


Lorsque cette propriété est définie sur [PlainText](../../markdownlistexportmode/), toutes les étiquettes de liste sont mises à jour à l'aide de [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) et exportées avec leurs valeurs réelles. De telles listes peuvent être non compatibles avec le format Markdown et seront reconnues comme du texte brut lors de l'importation dans ce cas.

Lorsque cette propriété est définie sur [MarkdownSyntax](../../markdownlistexportmode/), l'écrivain tente d'exporter les éléments de liste d'une manière qui permet de numéroter les éléments de liste en mode automatique avec Markdown.

## Exemples



Montre comment les éléments de la liste seront écrits dans le document markdown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Utilisez MarkdownListExportMode.PlainText ou MarkdownListExportMode.MarkdownSyntax pour exporter la liste.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Voir aussi

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
