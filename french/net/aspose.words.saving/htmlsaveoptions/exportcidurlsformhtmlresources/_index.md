---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words pour .NET
description: Découvrez comment ExportCidUrlsForMhtmlResources de HtmlSaveOptions améliore les documents MHTML en activant les URL CID pour les images, les polices et le CSS. Valeur par défaut : false.
type: docs
weight: 110
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

Spécifie s'il faut utiliser les URL CID (Content-ID) pour référencer les ressources (images, polices, CSS) incluses dans les documents MHTML . La valeur par défaut est`FAUX` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Remarques

Cette option affecte uniquement les documents enregistrés au format MHTML.

Par défaut, les ressources dans les documents MHTML sont référencées par nom de fichier (par exemple, « image.png »), qui sont comparées aux en-têtes « Content-Location » des parties MIME.

Cette option active une méthode alternative, où les références aux fichiers de ressources sont écrites sous forme d'URL CID (Content-ID) (par exemple, « cid:image.png ») et sont comparées aux en-têtes « Content-ID ».

En théorie, il ne devrait y avoir aucune différence entre les deux méthodes de référencement et chacune d'elles devrait fonctionner correctement dans n'importe quel navigateur ou agent de messagerie. En pratique, cependant, certains agents ne parviennent pas à récupérer les ressources par nom de fichier. Si votre navigateur ou agent de messagerie refuse de charger les ressources incluses dans un document MTHML (n'affiche pas les images ou ne charge pas les styles CSS), essayez d'exporter le document avec les URL CID.

## Exemples

Montre comment activer les ID de contenu pour les documents MHTML de sortie.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// La définition de cet indicateur remplacera les balises « Content-Location »
// avec des balises « Content-ID » pour chaque ressource du document d'entrée.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
