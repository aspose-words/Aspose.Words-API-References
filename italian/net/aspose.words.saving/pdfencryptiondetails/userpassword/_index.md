---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words per .NET
description: Scopri come la proprietà UserPassword migliora la sicurezza dei PDF richiedendo una password per l'accesso, garantendo così la protezione e la riservatezza dei tuoi documenti.
type: docs
weight: 40
url: /it/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Specifica la password utente richiesta per aprire il documento PDF crittografato.

```csharp
public string UserPassword { get; set; }
```

## Osservazioni

Sarà richiesta la password utente per aprire un documento PDF crittografato e visualizzarlo. Le autorizzazioni specificate in [`Permissions`](../permissions/) verrà applicata dal software di lettura.

La password utente può essere`null` o stringa vuota, in questo caso non verrà richiesta alcuna password all'utente quando apre il documento PDF. La password utente non può essere uguale alla password del proprietario.

## Esempi

Mostra come impostare le autorizzazioni su un documento PDF salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Estendi i permessi per consentire la modifica delle annotazioni.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Abilita la crittografia tramite la proprietà "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// Quando apriamo questo documento, dovremo fornire la password prima di accedere al suo contenuto.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Guarda anche

* class [PdfEncryptionDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
