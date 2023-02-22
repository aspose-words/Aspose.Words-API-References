---
title: Class PdfEncryptionDetails
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.PdfEncryptionDetails classe. Contiene i dettagli per la crittografia e le autorizzazioni di accesso per un documento PDF.
type: docs
weight: 5180
url: /it/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Contiene i dettagli per la crittografia e le autorizzazioni di accesso per un documento PDF.

```csharp
public class PdfEncryptionDetails
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/)(string, string) | Inizializza un'istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Specifica la password del proprietario per il documento PDF crittografato. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Specifica le operazioni consentite a un utente su un documento PDF crittografato. Il valore predefinito èDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Specifica la password utente richiesta per aprire il documento PDF crittografato. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


