---
title: FileFormatInfo.IsEncrypted
second_title: Aspose.Words per .NET API Reference
description: FileFormatInfo proprietà. RestituisceVERO se il documento è crittografato e richiede una password per essere aperto.
type: docs
weight: 30
url: /it/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Restituisce`VERO` se il documento è crittografato e richiede una password per essere aperto.

```csharp
public bool IsEncrypted { get; }
```

### Osservazioni

Questa proprietà esiste per aiutarti a ordinare i documenti crittografati da quelli che non lo sono. Se provi a caricare un documento crittografato utilizzando Aspose.Words senza fornire una password, verrà generata un'eccezione . È possibile utilizzare questa proprietà per rilevare se un documento richiede una password ed eseguire alcune azioni prima di caricare un documento, ad esempio richiedere all'utente una password.

### Esempi

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato e la crittografia del documento.

```csharp
Document doc = new Document();

// Configura un oggetto SaveOptions per crittografare il documento
// con una password quando lo salviamo, quindi salviamo il documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verifica il tipo di file del nostro documento e il suo stato di crittografia.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Guarda anche

* class [FileFormatInfo](../)
* spazio dei nomi [Aspose.Words](../../fileformatinfo/)
* assemblea [Aspose.Words](../../../)


