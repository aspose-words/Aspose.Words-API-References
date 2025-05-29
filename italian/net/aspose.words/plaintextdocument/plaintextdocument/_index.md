---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words per .NET
description: Crea senza sforzo documenti di testo semplice con il nostro costruttore PlainTextDocument. Approfitta del rilevamento automatico del formato file per un'integrazione perfetta!
type: docs
weight: 10
url: /it/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

Crea un documento di testo normale da un file. Rileva automaticamente il formato del file.

```csharp
public PlainTextDocument(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file da cui estrarre il testo. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentException | Il nome del file non può essere nullo o una stringa vuota. |

## Esempi

Mostra come caricare il contenuto di un documento Microsoft Word in testo normale.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Guarda anche

* class [PlainTextDocument](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

Crea un documento di testo normale da un file. Permette di specificare opzioni aggiuntive come una password di crittografia.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file da cui estrarre il testo. |
| loadOptions | LoadOptions | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Possono essere`null`. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentException | Il nome del file non può essere nullo o una stringa vuota. |

## Esempi

Mostra come caricare il contenuto di un documento Microsoft Word crittografato in testo normale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

Crea un documento di testo normale da un flusso. Rileva automaticamente il formato del file.

```csharp
public PlainTextDocument(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso da cui estrarre il testo. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentNullException | Il flusso non può essere nullo. |
| NotSupportedException | Il flusso non supporta la lettura o la ricerca. |
| ObjectDisposedException | Il flusso è un oggetto disposto. |

## Osservazioni

Il documento deve essere memorizzato all'inizio del flusso. Il flusso deve supportare il posizionamento casuale.

## Esempi

Mostra come caricare il contenuto di un documento Microsoft Word in testo normale utilizzando stream.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Guarda anche

* class [PlainTextDocument](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

Crea un documento di testo normale da un flusso. Permette di specificare opzioni aggiuntive come una password di crittografia.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso da cui estrarre il testo. |
| loadOptions | LoadOptions | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Possono essere`null`. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Il formato del documento non è riconosciuto o non è supportato. |
| [FileCorruptedException](../../filecorruptedexception/) | Il documento sembra danneggiato e non può essere caricato. |
| Exception | C'è un problema con il documento e dovrebbe essere segnalato agli sviluppatori di Aspose.Words. |
| IOException | C'è un'eccezione di input/output. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Il documento è crittografato e richiede una password per essere aperto, ma hai fornito una password errata. |
| ArgumentNullException | Il flusso non può essere nullo. |
| NotSupportedException | Il flusso non supporta la lettura o la ricerca. |
| ObjectDisposedException | Il flusso è un oggetto disposto. |

## Osservazioni

Il documento deve essere memorizzato all'inizio del flusso. Il flusso deve supportare il posizionamento casuale.

## Esempi

Mostra come caricare il contenuto di un documento Microsoft Word crittografato in testo normale utilizzando il flusso.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
