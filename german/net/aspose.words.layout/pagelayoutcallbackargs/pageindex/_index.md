---
title: PageLayoutCallbackArgs.PageIndex
second_title: Aspose.Words für .NET-API-Referenz
description: PageLayoutCallbackArgs eigendom. Ruft den 0basierten Index der Seite im Dokument ab auf die sich dieses Ereignis bezieht. Gibt einen negativen Wert zurück wenn keine zugeordnete Seite vorhanden ist oder wenn die Seite während des Reflows entfernt wurde.
type: docs
weight: 30
url: /de/net/aspose.words.layout/pagelayoutcallbackargs/pageindex/
---
## PageLayoutCallbackArgs.PageIndex property

Ruft den 0-basierten Index der Seite im Dokument ab, auf die sich dieses Ereignis bezieht. Gibt einen negativen Wert zurück, wenn keine zugeordnete Seite vorhanden ist oder wenn die Seite während des Reflows entfernt wurde.

```csharp
public int PageIndex { get; }
```

### Beispiele

Zeigt, wie Layoutänderungen mit einem Layout-Callback verfolgt werden.

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
/// und rendert eine Seite, auf der wir einen Seiten-Reflow durchführen, in ein Bild im lokalen Dateisystem.
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

* class [PageLayoutCallbackArgs](../)
* namensraum [Aspose.Words.Layout](../../pagelayoutcallbackargs/)
* Montage [Aspose.Words](../../../)


