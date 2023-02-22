---
title: PdfEncryptionDetails.UserPassword
second_title: Aspose.Words per .NET API Reference
description: PdfEncryptionDetails proprietà. Specifica la password utente richiesta per aprire il documento PDF crittografato.
type: docs
weight: 40
url: /it/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Specifica la password utente richiesta per aprire il documento PDF crittografato.

```csharp
public string UserPassword { get; set; }
```

### Osservazioni

La password utente sarà richiesta per aprire un documento PDF crittografato per la visualizzazione. Le autorizzazioni specificate in [`Permissions`](../permissions/) sarà imposto dal software del lettore.

La password utente può essere una stringa nulla o vuota, in questo caso non sarà richiesta alcuna password all'utente quando aprirà il documento PDF. La password dell'utente non può essere la stessa della password del proprietario.

### Esempi

Mostra come impostare le autorizzazioni su un documento PDF salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Inizia negando tutte le autorizzazioni.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Estendi i permessi per consentire la modifica delle annotazioni.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
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


