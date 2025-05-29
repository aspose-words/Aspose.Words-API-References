---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Layout.PageLayoutEvent, essenziale per ottimizzare gli eventi di layout di pagina durante il rendering e la creazione dei documenti. Migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 3820
url: /it/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Codice di evento generato durante la creazione e il rendering del modello di layout di pagina.

Il modello di layout di pagina viene creato in due fasi. Innanzitutto, la "fase di conversione", in cui il layout di pagina estrae il contenuto del documento e crea un grafico di oggetti. In secondo luogo, la "fase di riflusso", in cui le strutture vengono divise, unite e disposte in pagine.

A seconda dell'operazione che ha attivato la build, il modello di layout di pagina può essere o meno ulteriormente renderizzato in un formato di pagina fisso. Ad esempio, il calcolo del numero di pagine nel documento o l'aggiornamento dei campi non richiede il rendering, mentre l'esportazione in PDF sì.

```csharp
public enum PageLayoutEvent
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Valore predefinito |
| WatchDog | `1` | Corrisponde a un checkpoint nel codice che viene visitato spesso e che è adatto per interrompere il processo. |
| BuildStarted | `2` | La creazione del layout di pagina è iniziata. Attivato una volta. Questo è il primo evento che si verifica quando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) si chiama. |
| BuildFinished | `3` | La creazione del layout di pagina è terminata. Attivato una volta. Questo è l'ultimo evento che si verifica quando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) si chiama. |
| ConversionStarted | `4` | La conversione del modello del documento in layout di pagina è iniziata. Attivata una volta. Questo si verifica quando il modello di layout inizia a estrarre il contenuto del documento. |
| ConversionFinished | `5` | La conversione del modello del documento in layout di pagina è terminata. Attivato una volta. Questo si verifica quando il modello di layout smette di estrarre il contenuto del documento. |
| ReflowStarted | `6` | Il riadattamento del layout di pagina è iniziato. Attivato una volta. Questo si verifica quando il modello di layout inizia a riadattare il contenuto del documento. |
| ReflowFinished | `7` | Il riadattamento del layout di pagina è terminato. Attivato una volta. Questo si verifica quando il modello di layout interrompe il riadattamento del contenuto del documento. |
| PartReflowStarted | `8` | Il riflusso della pagina è iniziato. Nota che la pagina potrebbe rifluire più volte e che il riflusso potrebbe riavviarsi prima di essere completato. |
| PartReflowFinished | `9` | Il riflusso della pagina è terminato. Nota che la pagina potrebbe rifluire più volte e che il riflusso potrebbe riavviarsi prima del termine. |
| PartRenderingStarted | `10` | Il rendering della pagina è iniziato. Viene attivato una volta per pagina. |
| PartRenderingFinished | `11` | Il rendering della pagina è terminato. Questo viene attivato una volta per pagina. |

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

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
