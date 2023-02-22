---
title: HtmlFixedSaveOptions.PageHorizontalAlignment
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlFixedSaveOptions propriété. Spécifie lalignement horizontal des pages dans un document HTML. La valeur par défaut estHtmlFixedHorizontalPageAlignment.Center .
type: docs
weight: 110
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/
---
## HtmlFixedSaveOptions.PageHorizontalAlignment property

Spécifie l'alignement horizontal des pages dans un document HTML. La valeur par défaut est`HtmlFixedHorizontalPageAlignment.Center` .

```csharp
public HtmlFixedPageHorizontalAlignment PageHorizontalAlignment { get; set; }
```

### Exemples

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
* espace de noms [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Assemblée [Aspose.Words](../../../)


