---
title: Enum PdfPermissions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.PdfPermissions enum. Specifica le operazioni consentite a un utente su un documento PDF crittografato.
type: docs
weight: 5230
url: /it/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Specifica le operazioni consentite a un utente su un documento PDF crittografato.

```csharp
[Flags]
public enum PdfPermissions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| DisallowAll | `0` | Non consente tutte le operazioni sul documento PDF. Questo è il valore predefinito. |
| AllowAll | `FFFF` | Consente tutte le operazioni sul documento PDF. |
| ContentCopy | `10` | Copiare o altrimenti estrarre testo e grafica dal documento con operazioni diverse da quella controllata daContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Estrarre testo e grafica (a supporto dell'accessibilità agli utenti con disabilità o per altri scopi). |
| ModifyContents | `8` | Modifica il contenuto del documento con operazioni diverse da quelle controllate da ModifyAnnotations ,FillIn , eDocumentAssembly . |
| ModifyAnnotations | `20` | Aggiungere o modificare annotazioni di testo, compilare campi modulo interattivi e, seModifyContents is imposta, crea o modifica anche campi modulo interattivi (inclusi campi firma). |
| FillIn | `100` | Compila i campi del modulo interattivo esistenti (inclusi i campi della firma), anche seModifyContents è chiaro. |
| DocumentAssembly | `400` | Assembla il documento (inserisci, ruota o elimina le pagine e crea elementi di struttura del documento o immagini miniatura ), anche seModifyContents è chiaro. |
| Printing | `4` | Stampa il documento (possibilmente non al massimo livello di qualità, a seconda che HighResolutionPrintingè impostato anche). |
| HighResolutionPrinting | `804` | Stampa il documento su una rappresentazione da cui potrebbe essere generata una copia digitale fedele del contenuto PDF , sulla base di un algoritmo dipendente dall'implementazione. Quando questo flag è deselezionato (e Printing è impostato), la stampa deve essere limitata a una rappresentazione di basso livello dell'aspetto, possibilmente di qualità degradata. |

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


