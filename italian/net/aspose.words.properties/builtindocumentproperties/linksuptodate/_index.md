---
title: BuiltInDocumentProperties.LinksUpToDate
linktitle: LinksUpToDate
articleTitle: LinksUpToDate
second_title: Aspose.Words per .NET
description: Scopri la funzionalità LinksUpToDate di BuiltInDocumentProperties, che garantisce che i collegamenti ipertestuali del tuo documento siano sempre aggiornati e migliora l'affidabilità del tuo contenuto.
type: docs
weight: 200
url: /it/net/aspose.words.properties/builtindocumentproperties/linksuptodate/
---
## BuiltInDocumentProperties.LinksUpToDate property

Indica se i collegamenti ipertestuali in un documento sono aggiornati.

```csharp
public bool LinksUpToDate { get; set; }
```

## Osservazioni

Aspose.Words non aggiorna questa proprietà.

## Esempi

Mostra come lavorare con le proprietà del documento nella categoria "Contenuto".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Utilizzando le proprietà integrate,
    // possiamo trattare le statistiche del documento come il numero di parole/pagine/caratteri come metadati che possono essere consultati senza aprire il documento
    // È possibile accedere a queste proprietà facendo clic con il pulsante destro del mouse sul file in Esplora risorse e selezionando Proprietà > Dettagli > Contenuto
    // Se vogliamo visualizzare questi dati all'interno del documento, possiamo utilizzare campi come NUMPAGES, NUMWORDS, NUMCHARS ecc.
    // Inoltre, questi valori possono essere visualizzati anche in Microsoft Word andando su File > Proprietà > Proprietà avanzate > Statistiche
    // Conteggio delle pagine: la proprietà PageCount mostra il conteggio delle pagine in tempo reale e il suo valore può essere assegnato alla proprietà Pages

     // La proprietà "Pagine" memorizza il numero di pagine del documento.
    Assert.AreEqual(6, properties.Pages);

    // Le proprietà integrate "Parole", "Caratteri" e "CaratteriConSpazi" mostrano anche varie statistiche del documento,
    // ma dobbiamo chiamare il metodo "UpdateWordCount" sull'intero documento prima di poterci aspettare che contenga valori accurati.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Conta il numero di righe nel documento, quindi assegna il risultato alla proprietà incorporata "Lines".
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Assegna il numero di nodi Paragrafo nel documento alla proprietà incorporata "Paragrafi".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Ottieni una stima della dimensione del file del nostro documento tramite la proprietà integrata "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // Imposta un modello diverso per il nostro documento, quindi aggiorna manualmente la proprietà integrata "Template" per riflettere questa modifica.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" è una proprietà descrittiva incorporata.
    properties.ContentStatus = "Draft";

    // Al momento del salvataggio, la proprietà integrata "ContentType" conterrà il tipo MIME del formato di salvataggio dell'output.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Se il documento contiene dei link e sono tutti aggiornati, possiamo impostare la proprietà "LinksUpToDate" su "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Conta le righe in un documento.
/// Attraversa l'albero delle entità di layout del documento durante la costruzione,
/// conteggio delle entità di tipo "Linea" che contengono anche testo reale.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
