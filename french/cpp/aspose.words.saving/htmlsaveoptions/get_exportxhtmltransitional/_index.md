---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional method"
linktitle: "get_ExportXhtmlTransitional"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional méthode. Spécifie s'il faut écrire la déclaration DOCTYPE lors de l'enregistrement en HTML ou MHTML. Lorsque true, écrit une déclaration DOCTYPE dans le document avant l'élément racine. La valeur par défaut est false. Lors de l'enregistrement en EPUB ou HTML5 (Html5), la déclaration DOCTYPE est toujours écrite en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


Spécifie s'il faut écrire la déclaration DOCTYPE lors de l'enregistrement en HTML ou MHTML. Lorsque **true**, écrit une déclaration DOCTYPE dans le document avant l'élément racine. La valeur par défaut est **false**. Lors de l'enregistrement en EPUB ou HTML5 ([Html5](../../htmlversion/)), la déclaration DOCTYPE est toujours écrite.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## Remarques


Aspose.Words écrit toujours du HTML bien formé quel que soit ce paramètre.

Lorsque **true**, le début du document HTML de sortie ressemblera à ceci :


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words vise à produire du XHTML conformément à la spécification XHTML 1.0 Transitional, mais la sortie ne sera pas toujours valide par rapport à la DTD. Certaines structures d'un document Microsoft Word sont difficiles ou impossibles à mapper à un document qui serait valide selon le schéma XHTML. Par exemple, le XHTML n'autorise pas les listes imbriquées (une UL ne peut pas être imbriquée dans une autre UL), mais dans les documents Microsoft Word, les listes à plusieurs niveaux apparaissent assez souvent.

## Exemples



Montre comment afficher une en-tête DOCTYPE lors de la conversion de documents vers la norme Xhtml 1.0 transitional.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Notre document ne contiendra une en-tête de déclaration DOCTYPE que si nous avons défini le drapeau "ExportXhtmlTransitional" sur "true".
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html");
System::String newLine = System::Environment::get_NewLine();

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(System::String::Format(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{0}", newLine) + System::String::Format(u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{0}", newLine) + u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
