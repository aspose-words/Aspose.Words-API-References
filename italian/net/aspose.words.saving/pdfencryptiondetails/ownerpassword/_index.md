---
title: PdfEncryptionDetails.OwnerPassword
second_title: Aspose.Words per .NET API Reference
description: PdfEncryptionDetails proprietà. Specifica la password del proprietario per il documento PDF crittografato.
type: docs
weight: 20
url: /it/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Specifica la password del proprietario per il documento PDF crittografato.

```csharp
public string OwnerPassword { get; set; }
```

### Osservazioni

La password del proprietario consente all'utente di aprire un documento PDF crittografato senza alcuna restrizione di accesso specificata in[`Permissions`](../permissions/).

La password del proprietario non può essere uguale alla password dell'utente.

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

* class [PdfEncryptionDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfencryptiondetails/)
* assemblea [Aspose.Words](../../../)


