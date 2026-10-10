---
title: "Aspose::Words::Saving::MarkdownListExportMode énumération"
linktitle: "MarkdownListExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownListExportMode énumération. Spécifie comment les listes sont exportées en Markdown en C++."
type: docs
weight: 68000
url: /fr/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Spécifie comment les listes sont exportées vers Markdown.

```cpp
enum class MarkdownListExportMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| MarkdownSyntax | 0 | Exportez les éléments de liste compatibles avec la syntaxe Markdown. |
| PlainText | 1 | Exporter les éléments de la liste en texte brut. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
