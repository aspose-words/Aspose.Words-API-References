---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words per .NET
description: Scopri il costruttore PdfEncryptionDetails per inizializzare facilmente istanze di crittografia PDF sicure. Migliora la protezione dei tuoi documenti con il nostro potente strumento!
type: docs
weight: 10
url: /it/net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails(*string, string*) {#constructor}

Inizializza un'istanza di questa classe.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

### Guarda anche

* class [PdfEncryptionDetails](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## PdfEncryptionDetails(*string, string, [PdfPermissions](../../pdfpermissions/)*) {#constructor_1}

Inizializza un'istanza di questa classe.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword, PdfPermissions permissions)
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
