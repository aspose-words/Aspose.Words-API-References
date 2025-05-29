---
title: PageLayoutCallbackArgs Class
linktitle: PageLayoutCallbackArgs
articleTitle: PageLayoutCallbackArgs
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Layout.PageLayoutCallbackArgs pour une gestion efficace de la mise en page de vos documents. Améliorez votre flux de travail grâce à de puissantes fonctionnalités de notification.
type: docs
weight: 3810
url: /fr/net/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class

Un argument passé dans[`Notify`](../ipagelayoutcallback/notify/)

Pour en savoir plus, visitez le[Conversion au format de page fixe](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) article de documentation.

```csharp
public class PageLayoutCallbackArgs
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Document](../../aspose.words.layout/pagelayoutcallbackargs/document/) { get; } | Obtient le document. |
| [Event](../../aspose.words.layout/pagelayoutcallbackargs/event/) { get; } | Obtient l'événement. |
| [PageIndex](../../aspose.words.layout/pagelayoutcallbackargs/pageindex/) { get; } | Obtient l'index de base 0 de la page du document auquel cet événement se rapporte. Renvoie une valeur négative s'il n'y a pas de page associée ou si la page a été supprimée pendant la redistribution. |

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

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)
