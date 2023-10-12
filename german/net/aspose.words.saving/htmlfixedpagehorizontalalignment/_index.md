---
title: Enum HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.HtmlFixedPageHorizontalAlignment opsomming. Gibt die horizontale Ausrichtung für Seiten im ausgegebenen HTMLDokument an.
type: docs
weight: 5070
url: /de/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

Gibt die horizontale Ausrichtung für Seiten im ausgegebenen HTML-Dokument an.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Left | `0` | Seiten links ausrichten. |
| Center | `1` | Seiten zentrieren. Dies ist der Standardwert. |
| Right | `2` | Seiten rechts ausrichten. |

### Beispiele

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


