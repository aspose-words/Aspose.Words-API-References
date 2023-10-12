---
title: PdfSaveOptions.EncryptionDetails
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Ottiene o imposta i dettagli per crittografare il documento PDF di output.
type: docs
weight: 130
url: /it/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Ottiene o imposta i dettagli per crittografare il documento PDF di output.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

### Osservazioni

Il valore predefinito è`nullo` e il documento di output non verrà crittografato. Quando questa proprietà è impostata su valido[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, , il documento PDF di output verrà crittografato.

L'algoritmo di crittografia AES-128 viene utilizzato durante il salvataggio in conformità basata su PDF 1.7 (incluso PDF/UA-1). L'algoritmo di crittografia AES-256 viene utilizzato durante il salvataggio in conformità basata su PDF 2.0.

La crittografia è vietata dalla conformità PDF/A. Questa opzione verrà ignorata durante il salvataggio in PDF/A.

ContentCopyForAccessibility l'autorizzazione è richiesta dalla conformità PDF/UA se il documento di output è crittografato. Questa autorizzazione verrà utilizzata automaticamente durante il salvataggio in PDF/UA.

ContentCopyForAccessibility l'autorizzazione è deprecata nel formato PDF 2.0. Questa autorizzazione verrà ignorata durante il salvataggio in PDF 2.0.

### Esempi

Mostra come impostare le autorizzazioni su un documento PDF salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Estende i permessi per consentire la modifica delle annotazioni.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Abilita la crittografia tramite la proprietà "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// Quando apriremo questo documento, dovremo fornire la password prima di accedere al suo contenuto.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Guarda anche

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


