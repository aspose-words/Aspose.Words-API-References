---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText méthode"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText. Contrôle la façon dont les champs de formulaire déroulants sont enregistrés en HTML ou MHTML. La valeur par défaut est false en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Contrôle comment les champs de formulaire déroulants sont enregistrés en HTML ou MHTML. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Remarques


Lorsqu'il est défini sur **true**, il exporte les champs de formulaire déroulants en texte normal. Lorsqu'il est **false**, il exporte les champs de formulaire déroulants en tant qu'élément SELECT en HTML.

Lors de l'exportation vers EPUB, les champs de formulaire déroulants texte sont toujours enregistrés en texte en raison des exigences de ce format.

## Exemples



Montre comment faire en sorte que les champs de formulaire combo déroulant s'intègrent au texte du paragraphe lors de l'enregistrement en html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez un constructeur de document pour insérer une boîte combo avec la valeur "Two" sélectionnée.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// Le drapeau "ExportDropDownFormFieldAsText" de cet objet SaveOptions nous permet de
// contrôler la façon dont l'enregistrement du document en HTML traite les boîtes combo déroulantes.
// Le définir sur "true" convertira chaque boîte combo en texte simple
// qui affiche la valeur actuellement sélectionnée de la boîte combo, la figant ainsi.
// Le définir sur "false" préservera la fonctionnalité de la boîte combo en utilisant les balises <select> et <option>.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
