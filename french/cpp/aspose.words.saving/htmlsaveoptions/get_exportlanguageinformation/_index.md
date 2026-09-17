---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation"
linktitle: "get_ExportLanguageInformation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation. Spécifie si les informations de langue sont exportées vers le HTML, le MHTML ou l'EPUB. La valeur par défaut est false en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Spécifie si les informations de langue sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Remarques


Lorsque cette propriété est définie sur **true**, Aspose.Words génère l'attribut HTML **lang** sur les éléments du document qui spécifient la langue. Cela peut être nécessaire pour préserver la sémantique liée à la langue.

## Exemples



Montre comment préserver les informations de langue lors de l'enregistrement en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez le constructeur pour écrire du texte tout en le formatant dans différentes locales.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// Lors de l'enregistrement du document au format HTML, nous pouvons passer un objet SaveOptions
// pour soit préserver, soit supprimer la locale de chaque texte formaté.
// Si nous définissons le drapeau "ExportLanguageInformation" sur "true",
// le document HTML de sortie contiendra les locales dans les attributs "lang" des balises <span>.
// Si nous définissons le drapeau "ExportLanguageInformation" sur "false',
// le texte du document HTML de sortie ne contiendra aucune information de locale.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
