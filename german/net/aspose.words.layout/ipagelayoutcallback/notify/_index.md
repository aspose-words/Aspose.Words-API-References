---
title: IPageLayoutCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words für .NET
description: Entdecken Sie die iPageLayoutCallback-Benachrichtigungsmethode, um die Effizienz beim Erstellen und Rendern von Layouts zu verbessern. Optimieren Sie noch heute die Leistung Ihrer App!
type: docs
weight: 10
url: /de/net/aspose.words.layout/ipagelayoutcallback/notify/
---
## IPageLayoutCallback.Notify method

Dies wird aufgerufen, um über den Fortschritt beim Erstellen und Rendern des Layouts zu informieren.

```csharp
public void Notify(PageLayoutCallbackArgs args)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | PageLayoutCallbackArgs | Ein Argument des Ereignisses. |

## Bemerkungen

Eine von der Implementierung ausgelöste Ausnahme bricht den Layout-Erstellungsprozess ab.

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

* class [PageLayoutCallbackArgs](../../pagelayoutcallbackargs/)
* interface [IPageLayoutCallback](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
