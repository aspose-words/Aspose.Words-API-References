---
title: HtmlFixedSaveOptions.PageHorizontalAlignment
linktitle: PageHorizontalAlignment
articleTitle: PageHorizontalAlignment
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageHorizontalAlignment di HtmlFixedSaveOptions per controllare facilmente l'allineamento delle pagine nei documenti HTML. L'impostazione predefinita è Center per una presentazione ottimale.
type: docs
weight: 120
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/
---
## HtmlFixedSaveOptions.PageHorizontalAlignment property

Specifica l'allineamento orizzontale delle pagine in un documento HTML. Il valore predefinito èCenter .

```csharp
public HtmlFixedPageHorizontalAlignment PageHorizontalAlignment { get; set; }
```

## Esempi

Mostra come impostare l'allineamento orizzontale delle pagine quando si salva un documento in formato HTML.

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

### Guarda anche

* enum [HtmlFixedPageHorizontalAlignment](../../htmlfixedpagehorizontalalignment/)
* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
