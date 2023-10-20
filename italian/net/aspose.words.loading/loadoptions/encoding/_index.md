---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words per .NET
description: LoadOptions Encoding proprietà. Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML TXT o CHM se la codifica non è specificata allinterno del documento. Può esserenullo . Limpostazione predefinita ènullo  in C#.
type: docs
weight: 50
url: /it/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere`nullo` . L'impostazione predefinita è`nullo` .

```csharp
public Encoding Encoding { get; set; }
```

## Osservazioni

Questa proprietà viene utilizzata solo durante il caricamento di documenti HTML, TXT o CHM.

Se la codifica non è specificata all'interno del documento e questa proprietà lo è`nullo`il sistema proverà a rilevare automaticamente la codifica.

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
