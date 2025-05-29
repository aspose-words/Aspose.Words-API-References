---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words per .NET
description: Scopri la proprietà WebRequestTimeout di HtmlLoadOptions, che ti consente di personalizzare le impostazioni di timeout per prestazioni web ottimali. Il valore predefinito è 100 secondi.
type: docs
weight: 80
url: /it/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Numero di millisecondi di attesa prima che la richiesta web scada. Il valore predefinito è 100000 millisecondi (100 secondi).

```csharp
public int WebRequestTimeout { get; set; }
```

## Osservazioni

Numero di millisecondi che Aspose.Words attende per una risposta quando carica risorse esterne (immagini, fogli di stile) collegate nei documenti HTML e MHTML.

## Esempi

Mostra come impostare un limite di tempo per le richieste web quando si carica un documento con risorse esterne collegate tramite URL.

```csharp
public void WebRequestTimeout()
{
    // Crea un nuovo oggetto HtmlLoadOptions e verifica la soglia di timeout per una richiesta web.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // Quando si carica un documento HTML con risorse collegate esternamente tramite un URL di indirizzo web,
    // Aspose.Words interromperà le richieste web che non riescono a recuperare le risorse entro questo limite di tempo, in millisecondi.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Imposta un WarningCallback che registrerà tutti gli avvisi che si verificano durante il caricamento.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Carica tale documento e verifica che sia stata creata una forma con dati immagine.
    // Per caricare questa immagine collegata sarà necessaria una richiesta web, che dovrà essere completata entro il limite di tempo da noi stabilito.
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
    // Tuttavia, l'immagine sarà quella "x" rossa che solitamente indica le immagini mancanti.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Possiamo anche configurare un callback personalizzato per raccogliere eventuali avvisi dalle richieste web scadute.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Memorizza in un elenco tutti gli avvisi che si verificano durante un'operazione di caricamento di un documento.
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
