---
title: HtmlFixedPageHorizontalAlignment Enum
linktitle: HtmlFixedPageHorizontalAlignment
articleTitle: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.HtmlFixedPageHorizontalAlignment für die präzise Steuerung der Seitenausrichtung in Ihren HTML-Dokumenten. Verbessern Sie noch heute Ihre Dokumentformatierung!
type: docs
weight: 5820
url: /de/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

Gibt die horizontale Ausrichtung für Seiten im HTML-Ausgabedokument an.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Left | `0` | Seiten linksbündig ausrichten. |
| Center | `1` | Seiten zentrieren. Dies ist der Standardwert. |
| Right | `2` | Seiten rechtsbündig ausrichten. |

## Beispiele

Zeigt, wie die horizontale Ausrichtung von Seiten beim Speichern eines Dokuments im HTML-Format festgelegt wird.

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

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
