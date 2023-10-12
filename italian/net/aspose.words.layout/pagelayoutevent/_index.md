---
title: Enum PageLayoutEvent
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.PageLayoutEvent enum. Un codice di evento generato durante la creazione e il rendering del modello di layout di pagina.
type: docs
weight: 3370
url: /it/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Un codice di evento generato durante la creazione e il rendering del modello di layout di pagina.

Il modello di layout della pagina è costruito in due passaggi. Il primo, "passaggio di conversione", avviene quando il layout della pagina estrae il contenuto del documento e crea il grafico dell'oggetto. Il secondo, "passaggio di ridisposizione", avviene quando le strutture vengono divise, unite e disposte in pagine.

A seconda dell'operazione che ha attivato la creazione, il modello di layout della pagina può o meno essere ulteriormente renderizzato in un formato di pagina fisso. Ad esempio, il calcolo del numero di pagine nel documento o l'aggiornamento dei campi non richiede il rendering, mentre l'esportazione in Pdf sì.

```csharp
public enum PageLayoutEvent
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Valore predefinito |
| WatchDog | `1` | Corrisponde a un checkpoint nel codice che viene visitato spesso e che è adatto per interrompere il processo. |
| BuildStarted | `2` | La creazione del layout della pagina è iniziata. Attivato una volta. Questo è il primo evento che si verifica quando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) si chiama. |
| BuildFinished | `3` | La creazione del layout della pagina è terminata. Attivato una volta. Questo è l'ultimo evento che si verifica quando[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) si chiama. |
| ConversionStarted | `4` | La conversione del modello di documento nel layout di pagina è iniziata. Attivato una volta. Ciò si verifica quando il modello di layout inizia a estrarre il contenuto del documento. |
| ConversionFinished | `5` | La conversione del modello di documento nel layout di pagina è terminata. Attivato una volta. Ciò si verifica quando il modello di layout smette di estrarre il contenuto del documento. |
| ReflowStarted | `6` | Il riflusso del layout della pagina è iniziato. Attivato una volta. Si verifica quando il modello di layout inizia a ridisporre il contenuto del documento. |
| ReflowFinished | `7` | La ridisposizione del layout della pagina è terminata. Attivato una volta. Ciò si verifica quando il modello di layout smette di ridisporre il contenuto del documento. |
| PartReflowStarted | `8` | La ridisposizione della pagina è iniziata. Tieni presente che la pagina potrebbe scorrere più volte e che la ridisposizione potrebbe riavviarsi prima del termine. |
| PartReflowFinished | `9` | La ridisposizione della pagina è terminata. Tieni presente che la pagina potrebbe scorrere più volte e che la ridisposizione potrebbe riavviarsi prima del termine. |
| PartRenderingStarted | `10` | Il rendering della pagina è iniziato. Viene attivato una volta per pagina. |
| PartRenderingFinished | `11` | Il rendering della pagina è terminato. Viene attivato una volta per pagina. |

### Esempi

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

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)


