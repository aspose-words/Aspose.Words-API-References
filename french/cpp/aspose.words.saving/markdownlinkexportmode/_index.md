---
title: "Aspose::Words::Saving::MarkdownLinkExportMode enum"
linktitle: "MarkdownLinkExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownLinkExportMode enum. Spécifie comment les liens sont exportés en Markdown en C++."
type: docs
weight: 67000
url: /fr/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


Spécifie comment les liens sont exportés vers Markdown.

```cpp
enum class MarkdownLinkExportMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Auto | 0 | Détecter automatiquement le mode d'exportation pour chaque lien. |
| Inline | 1 | Exporter tous les liens en tant que blocs en ligne. |
| Référence | 2 | Exporter tous les liens en tant que blocs de référence. |


## Exemples



Montre comment les liens seront écrits dans le fichier .md.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// L'image sera écrite en tant que référence :
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// L'image sera écrite en ligne :
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
