---
title: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml"
linktitle: "get_ExportAsHtml"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml. Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut. La valeur par défaut est None en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_exportashtml/
---
## MarkdownSaveOptions::get_ExportAsHtml method


Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut. La valeur par défaut est [None](../../markdownexportashtml/).

```cpp
Aspose::Words::Saving::MarkdownExportAsHtml Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml() const
```


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

* Enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
