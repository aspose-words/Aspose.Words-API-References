---
title: PageLayoutCallbackArgs.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageIndex de PageLayoutCallbackArgs, qui fournit l'index de base 0 de la page du document concerné. Obtenez un suivi précis des pages et des informations sur la redistribution !
type: docs
weight: 30
url: /fr/net/aspose.words.layout/pagelayoutcallbackargs/pageindex/
---
## PageLayoutCallbackArgs.PageIndex property

Obtient l'index de base 0 de la page du document auquel cet événement se rapporte. Renvoie une valeur négative s'il n'y a pas de page associée ou si la page a été supprimée pendant la redistribution.

```csharp
public int PageIndex { get; }
```

## Exemples

Montre comment suivre les modifications de mise en page avec un rappel de mise en page.

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
/// Nous avertit lorsque nous enregistrons le document dans un format de page fixe
/// et restitue une page sur laquelle nous effectuons un reflow de page sur une image dans le système de fichiers local.
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

* class [PageLayoutCallbackArgs](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
