---
title: PageLayoutCallbackArgs.Event
second_title: Référence de l'API Aspose.Words pour .NET
description: PageLayoutCallbackArgs propriété. Obtient lévénement.
type: docs
weight: 20
url: /fr/net/aspose.words.layout/pagelayoutcallbackargs/event/
---
## PageLayoutCallbackArgs.Event property

Obtient l'événement.

```csharp
public PageLayoutEvent Event { get; }
```

### Exemples

Montre comment suivre les modifications de mise en page avec un rappel de mise en page.

```csharp
[Test]
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
/// Nous avertit lorsque nous enregistrons le document dans un format de page fixe
/// et affiche une page sur laquelle nous effectuons une redistribution de page vers une image dans le système de fichiers local.
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

### Voir également

* enum [PageLayoutEvent](../../pagelayoutevent/)
* class [PageLayoutCallbackArgs](../)
* espace de noms [Aspose.Words.Layout](../../pagelayoutcallbackargs/)
* Assemblée [Aspose.Words](../../../)


