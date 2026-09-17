---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup méthode"
linktitle: "get_ExportPageSetup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup méthode. Spécifie si la configuration de la mise en page est exportée vers HTML, MHTML ou EPUB. La valeur par défaut est false en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Spécifie si la configuration de page est exportée vers HTML, MHTML ou EPUB. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Remarques


Chaque [Section](../../../aspose.words/section/) du modèle de document Aspose.Words fournit les informations de configuration de la mise en page via la classe [PageSetup](../../../aspose.words/pagesetup/). Lorsque vous exportez un document au format HTML, il peut être nécessaire de conserver ces informations pour une utilisation ultérieure. En particulier, la configuration de la mise en page peut être importante pour le rendu sur des supports paginés (impression) ou pour la conversion ultérieure vers les formats natifs de Microsoft Word (DOCX, DOC, RTF, WML).

Dans la plupart des cas, le HTML est destiné à être visualisé dans les navigateurs où la pagination n’est pas effectuée. Ainsi, cette fonctionnalité est désactivée par défaut.

## Exemples



Montre comment décider de préserver les informations de structure de section/configuration de la mise en page lors de l’enregistrement au format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(Aspose::Words::PaperSize::A5);

// Lors de l'enregistrement du document au format HTML, nous pouvons passer un objet SaveOptions
// pour décider de préserver ou de supprimer les paramètres de configuration de la mise en page.
// Si nous définissons le drapeau "ExportPageSetup" sur "true", le document HTML généré contiendra notre configuration de mise en page.
// Si nous définissons le drapeau "ExportPageSetup" sur "false", l’opération d’enregistrement supprimera nos paramètres de mise en page
// pour la première section, et les deux sections auront l’aspect identique.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<style type=\"text/css\">") + u"@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div class=\"Section_1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
