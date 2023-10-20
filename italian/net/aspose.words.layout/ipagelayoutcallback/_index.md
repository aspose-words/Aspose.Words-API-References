---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words per .NET
description: Aspose.Words.Layout.IPageLayoutCallback interfaccia. Implementa questa interfaccia se desideri che il tuo metodo personalizzato venga chiamato durante la creazione e il rendering del modello di layout della pagina in C#.
type: docs
weight: 3310
url: /it/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Implementa questa interfaccia se desideri che il tuo metodo personalizzato venga chiamato durante la creazione e il rendering del modello di layout della pagina.

```csharp
public interface IPageLayoutCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | Viene richiamato per notificare la creazione del layout e l'avanzamento del rendering. |

## Osservazioni

L'utilizzo principale di questa interfaccia è consentire al codice dell'applicazione di interrompere il processo di compilazione.

È possibile creare un modello di layout di pagina solo per poche pagine all'inizio del documento, quindi interrompere il processo e visualizzare solo ciò che è già stato creato.

Tieni presente, tuttavia, che i risultati del rendering potrebbero non corrispondere a ciò che verrebbe visualizzato per ciascuna pagina se il processo fosse terminato.

Questa tecnica potrebbe non funzionare per tutti i documenti o potrebbe fallire completamente.

## Esempi

Mostra come tenere traccia delle modifiche al layout con un callback del layout.

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
/// Ci avvisa quando salviamo il documento in un formato di pagina fisso
/// ed esegue il rendering di una pagina su cui eseguiamo il reflow della pagina su un'immagine nel file system locale.
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

* property [Callback](../layoutoptions/callback/)
* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
