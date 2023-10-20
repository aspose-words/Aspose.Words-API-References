---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words per .NET
description: PdfEncryptionDetails UserPassword proprietà. Specifica la password utente richiesta per aprire il documento PDF crittografato in C#.
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

La password utente sarà richiesta per aprire un documento PDF crittografato per la visualizzazione. Le autorizzazioni specificate in [`Permissions`](../permissions/) verrà applicato dal software del lettore.

La password dell'utente può essere`nullo` oppure stringa vuota, in questo caso non verrà richiesta alcuna password all'utente all'apertura del documento PDF. La password dell'utente non può essere uguale alla password del proprietario.

## Esempi

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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
