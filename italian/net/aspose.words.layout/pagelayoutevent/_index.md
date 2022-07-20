---
title: PageLayoutEvent
second_title: Aspose.Words per .NET API Reference
description: Un codice di evento generato durante la creazione e il rendering del modello di layout di pagina.
type: docs
weight: 3170
url: /it/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Un codice di evento generato durante la creazione e il rendering del modello di layout di pagina.

Il modello di layout di pagina è costruito in due passaggi. Primo, "passo di conversione", questo è quando il layout di pagina estrae il contenuto del documento e crea un grafico oggetto. Secondo, "passo di ridisposizione", questo è quando le strutture vengono divise, unite e disposte nelle pagine.

A seconda dell'operazione che ha attivato la creazione, il modello di layout di pagina può essere ulteriormente renderizzato o meno in un formato di pagina fisso. Ad esempio, il calcolo del numero di pagine nel documento o l'aggiornamento dei campi non richiede il rendering, mentre l'esportazione in Pdf lo fa.

```csharp
public enum PageLayoutEvent
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Valore predefinito |
| WatchDog | `1` | Corrisponde a un checkpoint nel codice che viene spesso visitato e che è adatto per interrompere il processo. |
| BuildStarted | `2` | La costruzione del layout di pagina è iniziata. Lanciato una volta. Questo è il primo evento che si verifica quando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout) viene chiamato. |
| BuildFinished | `3` | La creazione del layout di pagina è terminata. Lanciato una volta. Questo è l'ultimo evento che si verifica quando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout) viene chiamato. |
| ConversionStarted | `4` | È iniziata la conversione del modello di documento in layout di pagina. Attivato una volta. Ciò si verifica quando il modello di layout inizia a estrarre il contenuto del documento. |
| ConversionFinished | `5` | La conversione del modello di documento in layout di pagina è terminata. Attivato una volta. Ciò si verifica quando il modello di layout smette di estrarre il contenuto del documento. |
| ReflowStarted | `6` | È iniziata la ridisposizione del layout di pagina. Attivato una volta. Ciò si verifica quando il modello di layout inizia a ridisporre il contenuto del documento. |
| ReflowFinished | `7` | Il ridisposizione del layout di pagina è terminato. Attivato una volta. Ciò si verifica quando il modello di layout interrompe la ridisposizione del contenuto del documento. |
| PartReflowStarted | `8` | La ridisposizione della pagina è iniziata. Si noti che la pagina potrebbe ridisporre più volte e che la ridisposizione potrebbe ricominciare prima che sia terminata. |
| PartReflowFinished | `9` | La ridisposizione della pagina è terminata. Si noti che la pagina potrebbe ridisporre più volte e che la ridisposizione potrebbe ricominciare prima che sia terminata. |
| PartRenderingStarted | `10` | Il rendering della pagina è iniziato. Viene attivato una volta per pagina. |
| PartRenderingFinished | `11` | Il rendering della pagina è terminato. Viene attivato una volta per pagina. |

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

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
