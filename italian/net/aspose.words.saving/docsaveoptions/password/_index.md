---
title: DocSaveOptions.Password
second_title: Aspose.Words per .NET API Reference
description: DocSaveOptions proprietà. Ottiene/imposta una password per crittografare il documento utilizzando il metodo di crittografia RC4.
type: docs
weight: 30
url: /it/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Ottiene/imposta una password per crittografare il documento utilizzando il metodo di crittografia RC4.

```csharp
public string Password { get; set; }
```

### Osservazioni

Per salvare il documento senza crittografia questa proprietà dovrebbe essere una stringa nulla o vuota.

### Esempi

Mostra come impostare le opzioni di salvataggio per i formati Microsoft Word precedenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Imposta una password che proteggerà il caricamento del documento da Microsoft Word o Aspose.Words.
// Nota che questo non crittografa in alcun modo il contenuto del documento.
options.Password = "MyPassword";

// Se il documento contiene una lista di distribuzione, possiamo conservarla durante il salvataggio impostando questo flag su true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Per poter caricare il documento,
// dovremo applicare la password specificata nell'oggetto DocSaveOptions in un oggetto LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [DocSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../docsaveoptions/)
* assemblea [Aspose.Words](../../../)


