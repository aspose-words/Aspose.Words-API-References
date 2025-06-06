---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.PdfPermissions per controllare l'accesso degli utenti ai PDF crittografati. Migliora la sicurezza e gestisci le operazioni sui documenti in modo efficace.
type: docs
weight: 6310
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
| ContentCopy | `10` | Copiare o altrimenti estrarre testo e grafica dal documento tramite operazioni diverse da quelle controllate daContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Estrarre testo e grafica (a supporto dell'accessibilità per gli utenti con disabilità o per altri scopi). |
| ModifyContents | `8` | Modificare il contenuto del documento tramite operazioni diverse da quelle controllate da ModifyAnnotations ,FillIn , EDocumentAssembly . |
| ModifyAnnotations | `20` | Aggiungere o modificare annotazioni di testo, compilare campi di moduli interattivi e, seModifyContents is imposta, crea o modifica anche i campi del modulo interattivo (inclusi i campi della firma). |
| FillIn | `100` | Compila i campi del modulo interattivo esistente (inclusi i campi della firma), anche seModifyContents è chiaro. |
| DocumentAssembly | `400` | Assemblare il documento (inserire, ruotare o eliminare pagine e creare elementi di struttura del documento o immagini in miniatura ), anche seModifyContents è chiaro. |
| Printing | `4` | Stampa il documento (eventualmente non al massimo livello di qualità, a seconda che HighResolutionPrinting è anche impostato). |
| HighResolutionPrinting | `804` | Stampa il documento in una rappresentazione da cui potrebbe essere generata una copia digitale fedele del contenuto del PDF, in base a un algoritmo dipendente dall'implementazione. Quando questo flag è deselezionato (e Printing è impostato), la stampa deve essere limitata a una rappresentazione di basso livello dell'aspetto, eventualmente di qualità degradata. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
