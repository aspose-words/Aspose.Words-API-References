---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Layout.PageLayoutEvent, essentielle pour optimiser les événements de mise en page lors du rendu et de la création de documents. Améliorez votre flux de travail dès aujourd'hui !
type: docs
weight: 3820
url: /fr/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Un code d'événement déclenché lors de la création et du rendu du modèle de mise en page.

Le modèle de mise en page est construit en deux étapes. Premièrement, « l'étape de conversion », c'est à ce moment que la mise en page extrait le contenu du document et crée un graphique d'objets. Deuxièmement, « l'étape de redistribution », c'est à ce moment que les structures sont divisées, fusionnées et organisées en pages.

Selon l'opération qui a déclenché la construction, le modèle de mise en page peut ou non être rendu dans un format de page fixe. Par exemple, le calcul du nombre de pages dans le document ou la mise à jour des champs ne nécessite pas de rendu, alors que l'exportation au format PDF le nécessite.

```csharp
public enum PageLayoutEvent
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Valeur par défaut |
| WatchDog | `1` | Correspond à un point de contrôle dans le code qui est souvent visité et qui convient pour interrompre le processus. |
| BuildStarted | `2` | La construction de la mise en page a commencé. Déclenché une fois. Il s'agit du premier événement qui se produit lorsque[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) s'appelle. |
| BuildFinished | `3` | La construction de la mise en page est terminée. Déclenché une fois. Il s'agit du dernier événement qui se produit lorsque[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) s'appelle. |
| ConversionStarted | `4` | La conversion du modèle de document en mise en page a commencé. Déclenché une fois. Cela se produit lorsque le modèle de mise en page commence à extraire le contenu du document. |
| ConversionFinished | `5` | La conversion du modèle de document en mise en page est terminée. Déclenché une fois. Ce problème survient lorsque le modèle de mise en page cesse d'extraire le contenu du document. |
| ReflowStarted | `6` | La redistribution de la mise en page a commencé. Déclenché une fois. Cela se produit lorsque le modèle de mise en page commence à redistribuer le contenu du document. |
| ReflowFinished | `7` | La redistribution de la mise en page est terminée. Déclenché une fois. Cela se produit lorsque le modèle de mise en page arrête de redistribuer le contenu du document. |
| PartReflowStarted | `8` | Le reflow de la page a commencé. Notez que la page peut reflow plusieurs fois et que le reflow peut redémarrer avant d'être terminé. |
| PartReflowFinished | `9` | Le reflow de la page est terminé. Notez que la page peut reflow plusieurs fois et que le reflow peut redémarrer avant d'être terminé. |
| PartRenderingStarted | `10` | Le rendu de la page a commencé. Ce message est déclenché une fois par page. |
| PartRenderingFinished | `11` | Le rendu de la page est terminé. Ce message est déclenché une fois par page. |

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
