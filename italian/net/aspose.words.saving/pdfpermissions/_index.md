---
title: Enum PdfPermissions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.PdfPermissions enum. Specifica le operazioni consentite a un utente su un documento PDF crittografato.
type: docs
weight: 5510
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
| ContentCopy | `10` | Copia o altrimenti estrae testo e grafica dal documento con operazioni diverse da quelle controllate daContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Estrai testo e grafica (a supporto dell'accessibilità per utenti con disabilità o per altri scopi). |
| ModifyContents | `8` | Modifica il contenuto del documento con operazioni diverse da quelle controllate da ModifyAnnotations ,FillIn , EDocumentAssembly . |
| ModifyAnnotations | `20` | Aggiungi o modifica annotazioni di testo, compila campi modulo interattivi e, seModifyContents is inoltre imposta, crea o modifica i campi del modulo interattivo (compresi i campi della firma). |
| FillIn | `100` | Compila i campi del modulo interattivo esistente (compresi i campi della firma), anche seModifyContents è chiaro. |
| DocumentAssembly | `400` | Assembla il documento (inserisci, ruota o elimina pagine e crea elementi della struttura del documento o immagini miniature ), anche seModifyContents è chiaro. |
| Printing | `4` | Stampa il documento (possibilmente non al massimo livello di qualità, a seconda se HighResolutionPrinting è impostato). |
| HighResolutionPrinting | `804` | Stampa il documento in una rappresentazione da cui è possibile generare una copia digitale fedele del contenuto PDF, in base a un algoritmo dipendente dall'implementazione. Quando questo flag è cancellato (e Printing è impostato), la stampa sarà limitata a una rappresentazione di basso livello dell'aspetto, possibilmente di qualità scadente. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


