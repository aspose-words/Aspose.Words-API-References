---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources méthode"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources méthode. Spécifie s'il faut utiliser des URL CID (Content-ID) pour référencer les ressources (images, polices, CSS) incluses dans les documents MHTML. La valeur par défaut est false en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


Spécifie s'il faut utiliser des URL CID (Content-ID) pour référencer les ressources (images, polices, CSS) incluses dans les documents MHTML. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Remarques


Cette option affecte uniquement les documents enregistrés au format MHTML.

Par défaut, les ressources dans les documents MHTML sont référencées par le nom de fichier (par exemple, "image.png"), qui sont comparées aux en-têtes "Content-Location" des parties MIME.

Cette option active une méthode alternative, où les références aux fichiers de ressources sont écrites sous forme d'URL CID (Content-ID) (par exemple, "cid:image.png") et sont comparées aux en-têtes "Content-ID".

En théorie, il ne devrait y avoir aucune différence entre les deux méthodes de référence et chacune d'elles devrait fonctionner correctement dans n'importe quel navigateur ou client de messagerie. En pratique, cependant, certains agents échouent à récupérer les ressources par nom de fichier. Si votre navigateur ou client de messagerie refuse de charger les ressources incluses dans un document MTHML (n'affiche pas les images ou ne charge pas les styles CSS), essayez d'exporter le document avec des URL CID.

## Exemples



Montre comment activer les ID de contenu pour les documents MHTML de sortie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Définir ce drapeau remplacera les balises "Content-Location"
// par des balises "Content-ID" pour chaque ressource du document d'entrée.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
