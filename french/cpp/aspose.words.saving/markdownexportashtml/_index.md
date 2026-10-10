---
title: "Aspose::Words::Saving::MarkdownExportAsHtml énum"
linktitle: "MarkdownExportAsHtml"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownExportAsHtml énum. Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut en C++."
type: docs
weight: 66500
url: /fr/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut.

```cpp
enum class MarkdownExportAsHtml
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Exportez tous les éléments en utilisant la syntaxe Markdown sans aucun HTML brut. |
| Tableaux | 1 | Exporter les tableaux en HTML brut. |
| NonCompatibleTables | 2 | Exporter les tableaux qui ne peuvent pas être correctement représentés en Markdown pur en HTML brut. |


## Exemples



Montre comment exporter un tableau vers Markdown en HTML brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Créer un tableau.
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
