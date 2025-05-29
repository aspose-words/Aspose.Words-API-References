---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words per .NET
description: Scopri la proprietà LoadOptions Encoding per gestire facilmente la codifica dei documenti HTML, TXT o CHM. Personalizza il caricamento dei contenuti per prestazioni ottimali!
type: docs
weight: 50
url: /it/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere`null` Il valore predefinito è`null` .

```csharp
public Encoding Encoding { get; set; }
```

## Osservazioni

Questa proprietà viene utilizzata solo quando si caricano documenti HTML, TXT o CHM.

Se la codifica non è specificata all'interno del documento e questa proprietà è`null`il sistema proverà a rilevare automaticamente la codifica.

## Esempi

Mostra come impostare la codifica con cui aprire un documento.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Carica il documento passando l'oggetto LoadOptions, quindi verifica il contenuto del documento.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
