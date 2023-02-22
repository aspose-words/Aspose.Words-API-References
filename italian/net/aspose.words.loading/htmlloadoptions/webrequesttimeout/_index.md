---
title: HtmlLoadOptions.WebRequestTimeout
second_title: Aspose.Words per .NET API Reference
description: HtmlLoadOptions proprietà. Il numero di millisecondi di attesa prima del timeout della richiesta Web. Il valore predefinito è 100000 millisecondi 100 secondi.
type: docs
weight: 70
url: /it/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Il numero di millisecondi di attesa prima del timeout della richiesta Web. Il valore predefinito è 100000 millisecondi (100 secondi).

```csharp
public int WebRequestTimeout { get; set; }
```

### Osservazioni

Il numero di millisecondi in cui Aspose.Words attende una risposta, durante il caricamento di risorse esterne (immagini, fogli di stile ) collegate in documenti HTML e MHTML.

### Esempi

Mostra come impostare un limite di tempo per le richieste Web durante il caricamento di un documento con risorse esterne collegate da URL.

```csharp
{
    // Crea un nuovo oggetto HtmlLoadOptions e verifica la sua soglia di timeout per una richiesta web.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // Quando si carica un documento HTML con risorse collegate esternamente da un URL di un indirizzo Web,
    // Aspose.Words interromperà le richieste Web che non riescono a recuperare le risorse entro questo limite di tempo, in millisecondi.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Imposta un WarningCallback che registrerà tutti gli avvisi che si verificano durante il caricamento.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Carica un tale documento e verifica che sia stata creata una forma con i dati dell'immagine.
    // Questa immagine collegata richiederà una richiesta Web per il caricamento, che dovrà essere completata entro il nostro limite di tempo.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Imposta un limite di timeout irragionevole e prova a caricare di nuovo il documento.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // Una richiesta web che non riesce a ottenere un'immagine entro il tempo limite produrrà comunque un'immagine.
    // Tuttavia, l'immagine sarà la 'x' rossa che comunemente indica immagini mancanti.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Possiamo anche configurare una richiamata personalizzata per raccogliere eventuali avvisi da richieste Web scadute.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Memorizza tutti gli avvisi che si verificano durante un'operazione di caricamento del documento in un elenco.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Guarda anche

* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../htmlloadoptions/)
* assemblea [Aspose.Words](../../../)


