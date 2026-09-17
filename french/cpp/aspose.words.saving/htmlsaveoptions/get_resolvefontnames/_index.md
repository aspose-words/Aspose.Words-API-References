---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames méthode"
linktitle: "get_ResolveFontNames"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames méthode. Spécifie si les noms de familles de polices utilisés dans le document sont résolus et substitués selon FontSettings lors de l'écriture dans des formats basés sur HTML en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Spécifie si les noms de familles de polices utilisés dans le document sont résolus et substitués selon [FontSettings](../../../aspose.words/document/get_fontsettings/) lors de l'écriture dans des formats basés sur HTML.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Remarques


Par défaut, cette option est définie sur **false** et les noms de familles de polices sont écrits dans le HTML tels qu'ils sont spécifiés dans les documents source. Ainsi, [FontSettings](../../../aspose.words/document/get_fontsettings/) sont ignorés et aucune résolution ou substitution des noms de familles de polices n'est effectuée.

Si cette option est définie sur **true**, Aspose.Words utilise [FontSettings](../../../aspose.words/document/get_fontsettings/) pour résoudre chaque nom de famille de police spécifié dans un document source en le remplaçant par le nom d'une famille de polices disponible, en effectuant la substitution de police si nécessaire.

## Exemples



Montre comment résoudre tous les noms de polices avant de les écrire en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Ce document contient du texte qui mentionne une police que nous ne possédons pas.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// Si nous n'avons aucun moyen d'obtenir cette police, et que nous voulons pouvoir afficher tout le texte
// dans ce document dans un HTML de sortie, nous pouvons la substituer par une autre police.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// Par défaut, cette option est définie sur 'False' et Aspose.Words écrit les noms de police tels qu'ils sont spécifiés dans le document source
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
