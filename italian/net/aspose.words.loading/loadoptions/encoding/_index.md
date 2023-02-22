---
title: LoadOptions.Encoding
second_title: Aspose.Words per .NET API Reference
description: LoadOptions proprietà. Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML TXT o CHM se la codifica non è specificata allinterno del documento. Può essere nullo. Il valore predefinito è null.
type: docs
weight: 50
url: /it/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere nullo. Il valore predefinito è null.

```csharp
public Encoding Encoding { get; set; }
```

### Osservazioni

Questa proprietà viene utilizzata solo durante il caricamento di documenti HTML, TXT o CHM.

Se la codifica non è specificata all'interno del documento e questa proprietà lo è`nullo`, il sistema proverà a rilevare automaticamente la codifica.

### Esempi

Mostra come impostare la codifica con cui aprire un documento.

```csharp
// Un oggetto FileFormatInfo rileverà questo file come codificato in qualcosa di diverso da UTF-7.
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Encoded in UTF-7.txt");

Assert.AreNotEqual(Encoding.UTF7, fileFormatInfo.Encoding);

// Se carichiamo il documento senza configurazioni di caricamento, Aspose.Words rileverà la sua codifica come UTF-8.
Document doc = new Document(MyDir + "Encoded in UTF-7.txt");

// Il contenuto, analizzato in UTF-8, crea una stringa valida.
// Tuttavia, sapendo che il file è in UTF-7, possiamo vedere che il risultato non è corretto.
Assert.AreEqual("Hello world+ACE-", doc.ToString(SaveFormat.Text).Trim());

// In casi di codifica ambigua come questa, possiamo impostare una specifica variante di codifica
// per analizzare il file all'interno di un oggetto LoadOptions.
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.UTF7
};

// Carica il documento passando l'oggetto LoadOptions, quindi verifica il contenuto del documento.
doc = new Document(MyDir + "Encoded in UTF-7.txt", loadOptions);

Assert.AreEqual("Hello world!", doc.ToString(SaveFormat.Text).Trim());
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)


