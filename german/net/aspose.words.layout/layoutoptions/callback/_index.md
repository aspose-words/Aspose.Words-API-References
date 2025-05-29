---
title: LayoutOptions.Callback
linktitle: Callback
articleTitle: Callback
second_title: Aspose.Words für .NET
description: Entdecken Sie die LayoutOptions Callback-Eigenschaft zur einfachen Verwaltung von IPageLayoutCallback für eine erweiterte Seitenlayoutanpassung und ein verbessertes Benutzererlebnis.
type: docs
weight: 20
url: /de/net/aspose.words.layout/layoutoptions/callback/
---
## LayoutOptions.Callback property

Ruft ab oder legt fest[`IPageLayoutCallback`](../../ipagelayoutcallback/) Implementierung, die vom Seitenlayoutmodell verwendet wird.

```csharp
public IPageLayoutCallback Callback { get; set; }
```

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

* interface [IPageLayoutCallback](../../ipagelayoutcallback/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
