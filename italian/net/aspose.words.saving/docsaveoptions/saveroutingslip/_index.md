---
title: DocSaveOptions.SaveRoutingSlip
second_title: Aspose.Words per .NET API Reference
description: DocSaveOptions proprietà. Quandofalso  I dati RoutingSlip non vengono salvati nel documento di output. Il valore predefinito è VERO .
type: docs
weight: 60
url: /it/net/aspose.words.saving/docsaveoptions/saveroutingslip/
---
## DocSaveOptions.SaveRoutingSlip property

Quando`falso` , I dati RoutingSlip non vengono salvati nel documento di output. Il valore predefinito è **VERO** .

```csharp
public bool SaveRoutingSlip { get; set; }
```

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


