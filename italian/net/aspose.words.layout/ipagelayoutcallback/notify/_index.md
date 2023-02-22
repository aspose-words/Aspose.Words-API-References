---
title: IPageLayoutCallback.Notify
second_title: Aspose.Words per .NET API Reference
description: IPageLayoutCallback metodo. Viene chiamato per notificare lavanzamento della creazione del layout e del rendering.
type: docs
weight: 10
url: /it/net/aspose.words.layout/ipagelayoutcallback/notify/
---
## IPageLayoutCallback.Notify method

Viene chiamato per notificare l'avanzamento della creazione del layout e del rendering.

```csharp
public void Notify(PageLayoutCallbackArgs args)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| args | PageLayoutCallbackArgs | Un argomento dell'evento. |

### Osservazioni

L'eccezione generata dall'implementazione interrompe il processo di compilazione del layout.

### Esempi

Mostra come tenere traccia delle modifiche al layout con una richiamata del layout.

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
/// Avvisa quando salviamo il documento in un formato pagina fisso
/// ed esegue il rendering di una pagina su cui eseguiamo un riflusso della pagina in un'immagine nel file system locale.
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

### Guarda anche

* class [PageLayoutCallbackArgs](../../pagelayoutcallbackargs/)
* interface [IPageLayoutCallback](../)
* spazio dei nomi [Aspose.Words.Layout](../../ipagelayoutcallback/)
* assemblea [Aspose.Words](../../../)


