---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words per .NET
description: Personalizza il layout del tuo documento con l'interfaccia Aspose.Words.Layout.IPageLayoutCallback. Migliora il rendering con i tuoi metodi per risultati ottimali.
type: docs
weight: 3760
url: /it/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Implementa questa interfaccia se vuoi che venga chiamato il tuo metodo personalizzato durante la compilazione e il rendering del modello di layout di pagina.

```csharp
public interface IPageLayoutCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | Viene chiamato per notificare l'avanzamento della creazione del layout e del rendering. |

## Osservazioni

L'uso principale di questa interfaccia è consentire al codice dell'applicazione di interrompere il processo di compilazione.

È possibile creare un modello di layout di pagina solo per alcune pagine all'inizio del documento, quindi interrompere il processo ed eseguire il rendering solo di ciò che è già stato creato.

Tieni presente, tuttavia, che i risultati del rendering potrebbero non corrispondere a quanto verrebbe renderizzato per ciascuna pagina se il processo fosse terminato.

Questa tecnica potrebbe non funzionare per tutti i documenti o potrebbe fallire completamente.

## Esempi

Mostra come tenere traccia delle modifiche al layout con un callback di layout.

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
/// e visualizza una pagina su cui eseguiamo un reflow di pagina in un'immagine nel file system locale.
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
