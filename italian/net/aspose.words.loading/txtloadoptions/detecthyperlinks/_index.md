---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: Aspose.Words per .NET
description: Scopri come la proprietà DetectHyperlinks di TxtLoadOptions migliora l'elaborazione del testo rilevando i collegamenti ipertestuali, migliorando l'accuratezza dei dati. Il valore predefinito è "false".
type: docs
weight: 30
url: /it/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

Specifica se rilevare i collegamenti ipertestuali nel testo. Il valore predefinito è`falso` .

```csharp
public bool DetectHyperlinks { get; set; }
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
