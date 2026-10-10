---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix méthode"
linktitle: "get_CssClassNamePrefix"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix méthode. Spécifie un préfixe qui est ajouté à tous les noms de classes CSS. La valeur par défaut est une chaîne vide et les noms de classes CSS générés n'ont aucun préfixe commun en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


Spécifie un préfixe qui est ajouté à tous les noms de classes CSS. La valeur par défaut est une chaîne vide et les noms de classes CSS générés n'ont aucun préfixe commun.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## Remarques


Si cette valeur n'est pas vide, toutes les classes CSS générées par Aspose.Words commenceront par le préfixe spécifié. Cela peut être utile, par exemple, si vous ajoutez du CSS personnalisé aux documents générés et que vous souhaitez éviter les conflits de noms de classes.

Si la valeur n'est pas **null** ou vide, elle doit être un identifiant CSS valide.

## Exemples



Montre comment enregistrer un document en HTML et ajouter un préfixe à tous ses noms de classes CSS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
