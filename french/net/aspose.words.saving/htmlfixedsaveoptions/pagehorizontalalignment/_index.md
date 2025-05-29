---
title: HtmlFixedSaveOptions.PageHorizontalAlignment
linktitle: PageHorizontalAlignment
articleTitle: PageHorizontalAlignment
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlFixedSaveOptions PageHorizontalAlignment pour contrôler facilement l'alignement des pages dans les documents HTML. La valeur par défaut est définie sur Centre pour une présentation optimale.
type: docs
weight: 120
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/
---
## HtmlFixedSaveOptions.PageHorizontalAlignment property

Spécifie l'alignement horizontal des pages dans un document HTML. La valeur par défaut estCenter .

```csharp
public HtmlFixedPageHorizontalAlignment PageHorizontalAlignment { get; set; }
```

## Exemples

Montre comment définir l'alignement horizontal des pages lors de l'enregistrement d'un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    PageHorizontalAlignment = pageHorizontalAlignment
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case HtmlFixedPageHorizontalAlignment.Center:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Left:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Right:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }").Success);
        break;
}
```

### Voir également

* enum [HtmlFixedPageHorizontalAlignment](../../htmlfixedpagehorizontalalignment/)
* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
