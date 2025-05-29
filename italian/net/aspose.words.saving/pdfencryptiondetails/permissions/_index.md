---
title: PdfEncryptionDetails.Permissions
linktitle: Permissions
articleTitle: Permissions
second_title: Aspose.Words per .NET
description: Scopri la proprietà Permessi di PdfEncryptionDetails, che definisce le operazioni utente sui PDF crittografati. Sblocca la gestione sicura dei documenti con un accesso personalizzabile!
type: docs
weight: 30
url: /it/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Specifica le operazioni consentite a un utente su un documento PDF crittografato. Il valore predefinito èDisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
