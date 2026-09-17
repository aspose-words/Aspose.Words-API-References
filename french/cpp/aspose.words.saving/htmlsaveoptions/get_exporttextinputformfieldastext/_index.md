---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText méthode"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText méthode. Contrôle la façon dont les champs de formulaire de saisie de texte sont enregistrés en HTML ou MHTML. La valeur par défaut est false en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Contrôle la façon dont les champs de formulaire de saisie de texte sont enregistrés en HTML ou MHTML. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Remarques


Lorsqu'il est défini sur **true**, exporte les champs de formulaire de saisie de texte en texte normal. Lorsqu'il est **false**, exporte les champs de formulaire de saisie de texte Word en éléments INPUT dans HTML.

Lors de l'exportation vers EPUB, les champs de formulaire de saisie de texte sont toujours enregistrés en texte en raison des exigences de ce format.

## Exemples



Montre comment spécifier le dossier pour stocker les images liées après l'enregistrement au format .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Définissez une option pour exporter les champs de formulaire en texte brut au lieu d'éléments d'entrée HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
