---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words per .NET
description: HtmlLoadOptions WebRequestTimeout proprietà. Il numero di millisecondi di attesa prima che la richiesta Web scada. Il valore predefinito è 100000 millisecondi 100 secondi in C#.
type: docs
weight: 70
url: /it/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Il numero di millisecondi di attesa prima che la richiesta Web scada. Il valore predefinito è 100000 millisecondi (100 secondi).

```csharp
public int WebRequestTimeout { get; set; }
```

## Osservazioni

Il numero di millisecondi che Aspose.Words attende una risposta, durante il caricamento di risorse esterne (immagini, fogli style ) collegate in documenti HTML e MHTML.

## Esempi

Mostra come impostare un limite di tempo per le richieste web durante il caricamento di un documento con risorse esterne collegate da URL.

```csharp
public void WebRequestTimeout()
{
    // Crea un nuovo oggetto HtmlLoadOptions e verifica la soglia di timeout per una richiesta web.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // Quando si carica un documento Html con risorse collegate esternamente da un URL di indirizzo web,
    // Aspose.Words interromperà le richieste web che non riescono a recuperare le risorse entro questo limite di tempo, in millisecondi.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Imposta un WarningCallback che registrerà tutti gli avvisi che si verificano durante il caricamento.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Carica un documento di questo tipo e verifica che sia stata creata una forma con dati immagine.
    // Questa immagine collegata richiederà il caricamento di una richiesta web, che dovrà essere completata entro il nostro limite di tempo.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Imposta un limite di timeout irragionevole e prova a caricare nuovamente il documento.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // Una richiesta web che non riesce a ottenere un'immagine entro il limite di tempo produrrà comunque un'immagine.
    // Tuttavia, l'immagine sarà la "x" rossa che comunemente indica le immagini mancanti.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Possiamo anche configurare una richiamata personalizzata per raccogliere eventuali avvisi provenienti da richieste web scadute.
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
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
