---
title: HtmlFixedPageHorizontalAlignment Enum
linktitle: HtmlFixedPageHorizontalAlignment
articleTitle: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.HtmlFixedPageHorizontalAlignment per un controllo preciso dell'allineamento delle pagine nei tuoi documenti HTML. Migliora la formattazione dei tuoi documenti oggi stesso!
type: docs
weight: 5820
url: /it/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

Specifica l'allineamento orizzontale per le pagine nel documento HTML di output.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Left | `0` | Allinea le pagine a sinistra. |
| Center | `1` | Pagine centrali. Questo è il valore predefinito. |
| Right | `2` | Allinea le pagine a destra. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
