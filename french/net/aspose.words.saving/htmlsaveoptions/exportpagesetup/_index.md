---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ExportPageSetup propriété. Spécifie si la mise en page est exportée au format HTML MHTML ou EPUB. La valeur par défaut estFAUX  en C#.
type: docs
weight: 220
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Spécifie si la mise en page est exportée au format HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Remarques

Chaque[`Section`](../../../aspose.words/section/) dans le modèle de document Aspose.Words fournit des informations de configuration de page via[`PageSetup`](../../../aspose.words/pagesetup/) classe. Lorsque vous exportez un document au format HTML, vous devrez peut-être conserver ces informations pour une utilisation ultérieure. En particulier, la mise en page peut être importante pour le rendu sur un support paginé (impression) ou la conversion ultérieure vers les formats de fichiers natifs Microsoft Word (DOCX, DOC, RTF, WML).

Dans la plupart des cas, le HTML est destiné à être affiché dans des navigateurs où la pagination n'est pas effectuée. Cette feature est donc inactive par défaut.

## Exemples

Montre comment décider de conserver ou non les informations sur la structure des sections/la mise en page lors de l'enregistrement au format HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// Lors de l'enregistrement du document au format HTML, nous pouvons passer un objet SaveOptions
// pour décider de conserver ou de supprimer les paramètres de mise en page.
// Si nous définissons l'indicateur "ExportPageSetup" sur "true", le document HTML de sortie contiendra notre configuration de mise en page.
// Si nous définissons l'indicateur "ExportPageSetup" sur "false", l'opération de sauvegarde ignorera nos paramètres de mise en page
// pour la première section, et les deux sections seront identiques.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
