---
title: Interface IPageLayoutCallback
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.IPageLayoutCallback interfaccia. Implementa questa interfaccia se desideri che il tuo metodo personalizzato venga chiamato durante la creazione e il rendering del modello di layout di pagina.
type: docs
weight: 3110
url: /it/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Implementa questa interfaccia se desideri che il tuo metodo personalizzato venga chiamato durante la creazione e il rendering del modello di layout di pagina.

```csharp
public interface IPageLayoutCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(PageLayoutCallbackArgs) | Viene chiamato per notificare l'avanzamento della creazione del layout e del rendering. |

### Osservazioni

L'uso principale di questa interfaccia è consentire al codice dell'applicazione di interrompere il processo di compilazione.

È possibile costruire un modello di layout di pagina solo per poche pagine all'inizio del documento, quindi interrompere il processo ed eseguire il rendering solo di ciò che è già stato creato.

Nota, tuttavia, che i risultati del rendering potrebbero non corrispondere a ciò che verrebbe visualizzato per ciascuna pagina se il processo fosse terminato.

Questa tecnica potrebbe non funzionare per tutti i documenti o potrebbe non riuscire completamente.

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

* property [Callback](../layoutoptions/callback/)
* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)


