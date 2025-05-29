---
title: PageLayoutCallbackArgs Class
linktitle: PageLayoutCallbackArgs
articleTitle: PageLayoutCallbackArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Layout.PageLayoutCallbackArgs für effizientes Dokumentlayoutmanagement. Verbessern Sie Ihren Workflow mit leistungsstarken Benachrichtigungsfunktionen.
type: docs
weight: 3810
url: /de/net/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class

Ein Argument, das übergeben wurde an[`Notify`](../ipagelayoutcallback/notify/)

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Festseitenformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

```csharp
public class PageLayoutCallbackArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.layout/pagelayoutcallbackargs/document/) { get; } | Ruft das Dokument ab. |
| [Event](../../aspose.words.layout/pagelayoutcallbackargs/event/) { get; } | Ruft das Ereignis ab. |
| [PageIndex](../../aspose.words.layout/pagelayoutcallbackargs/pageindex/) { get; } | Ruft den 0-basierten Index der Seite im Dokument ab, auf das sich dieses Ereignis bezieht. Gibt einen negativen Wert zurück, wenn keine zugehörige Seite vorhanden ist oder wenn die Seite während des Neuflusses entfernt wurde. |

## Beispiele

Zeigt, wie Layoutänderungen mit einem Layout-Rückruf verfolgt werden.

```csharp
public void PageLayoutCallback()
{
    Document doc = new Document();
    doc.BuiltInDocumentProperties.Title = "My Document";

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");

    doc.LayoutOptions.Callback = new RenderPageLayoutCallback();
    doc.UpdatePageLayout();

    doc.Save(ArtifactsDir + "Layout.PageLayoutCallback.pdf");
}

/// <summary>
/// Benachrichtigt uns, wenn wir das Dokument in einem festen Seitenformat speichern
/// und rendert eine Seite, auf der wir einen Seitenumbruch in ein Bild im lokalen Dateisystem durchführen.
/// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
    public void Notify(PageLayoutCallbackArgs a)
    {
        switch (a.Event)
        {
            case PageLayoutEvent.PartReflowFinished:
                NotifyPartFinished(a);
                break;
            case PageLayoutEvent.ConversionFinished:
                NotifyConversionFinished(a);
                break;
        }
    }

    private void NotifyPartFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Part at page {a.PageIndex + 1} reflow.");
        RenderPage(a, a.PageIndex);
    }

    private void NotifyConversionFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Document \"{a.Document.BuiltInDocumentProperties.Title}\" converted to page format.");
    }

    private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
    {
        ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png) { PageSet = new PageSet(pageIndex) };

        using (FileStream stream =
            new FileStream(ArtifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
                FileMode.Create))
            a.Document.Save(stream, saveOptions);
    }

    private int mNum;
}
```

### Siehe auch

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
