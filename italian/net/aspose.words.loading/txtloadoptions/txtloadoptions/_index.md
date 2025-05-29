---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore TxtLoadOptions! Inizializza facilmente con valori predefiniti e semplifica il processo di caricamento dei dati per prestazioni migliori.
type: docs
weight: 10
url: /it/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Inizializza una nuova istanza di questa classe con valori predefiniti.

```csharp
public TxtLoadOptions()
```

## Esempi

Mostra come leggere e visualizzare i collegamenti ipertestuali.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Carica il documento con i collegamenti ipertestuali.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Stampa il testo dei collegamenti ipertestuali.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Guarda anche

* class [TxtLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
