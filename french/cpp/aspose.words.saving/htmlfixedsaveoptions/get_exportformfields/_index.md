---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields méthode"
linktitle: "get_ExportFormFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields méthode. Obtient ou définit l'indication de savoir si les champs de formulaire sont exportés en tant qu'éléments interactifs (en tant que balise ''input'') plutôt que convertis en texte ou graphiques en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Obtient ou définit l'indication de savoir si les champs de formulaire sont exportés en tant qu'éléments interactifs (comme la balise 'input') plutôt que convertis en texte ou graphiques.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Exemples



Montre comment exporter des champs de formulaire vers Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// Lorsque nous exportons un document avec des champs de formulaire vers .html,
// il existe deux manières dont Aspose.Words peut exporter les champs de formulaire.
// Définir le drapeau "ExportFormFields" sur "true" les exportera en tant qu'objets interactifs.
// Définir ce drapeau sur "false" affichera les champs de formulaire en texte brut.
// Cela les figera à leur valeur actuelle et empêchera le lecteur de notre document HTML
// de pouvoir interagir avec eux.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## Voir aussi

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
