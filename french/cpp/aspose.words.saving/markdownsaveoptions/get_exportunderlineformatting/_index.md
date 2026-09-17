---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting méthode"
linktitle: "get_ExportUnderlineFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting méthode. Obtient ou définit une valeur booléenne indiquant s'il faut exporter le format de texte souligné sous forme d'une séquence de deux caractères plus \\\"++\\\". La valeur par défaut est false en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Obtient ou définit une valeur booléenne indiquant s'il faut exporter le format de texte souligné sous forme d'une séquence de deux caractères plus "++". La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Exemples



Montre comment exporter le format de soulignement en ++.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## Voir aussi

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
