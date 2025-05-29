---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words per .NET
description: Scopri se il tuo documento è sicuro con la proprietà FileFormatInfo IsEncrypted, che restituisce true per i file crittografati per i quali è necessaria una password di accesso.
type: docs
weight: 40
url: /it/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Restituisce`VERO` se il documento è crittografato e richiede una password per aprirlo.

```csharp
public bool IsEncrypted { get; }
```

## Osservazioni

Questa proprietà esiste per aiutarti a distinguere i documenti crittografati da quelli non crittografati. Se tenti di caricare un documento crittografato utilizzando Aspose.Words senza fornire una password, verrà generata un'eccezione . Puoi utilizzare questa proprietà per rilevare se un documento richiede una password e intraprendere un'azione prima di caricare un documento, ad esempio richiedere una password all'utente.

## Esempi

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato e la crittografia del documento.

```csharp
Document doc = new Document();

// Configura un oggetto SaveOptions per crittografare il documento
// con una password quando lo salviamo, e poi salviamo il documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verificare il tipo di file del nostro documento e il suo stato di crittografia.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Guarda anche

* class [FileFormatInfo](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
