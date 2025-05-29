---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Settings.WriteProtection per gestire facilmente le impostazioni di protezione da scrittura dei documenti e migliorarne la sicurezza.
type: docs
weight: 6800
url: /it/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Specifica le impostazioni di protezione da scrittura per un documento.

Per saperne di più, visita il[Proteggere o crittografare un documento](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) articolo di documentazione.

```csharp
public class WriteProtection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Restituisce`VERO` quando è impostata una password di protezione da scrittura. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Specifica se l'autore del documento ha raccomandato di aprirlo in sola lettura. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Imposta la password di protezione da scrittura per il documento. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | Restituisce`VERO` se la password specificata è la stessa della password di protezione da scrittura con cui è stato protetto il documento. Se il documento non è protetto da scrittura con password, allora restituisce`falso` . |

## Osservazioni

La protezione da scrittura specifica se l'autore ha raccomandato che il documento venga aperto in sola lettura e/o che venga richiesta una password per modificarlo.

La protezione da scrittura è diversa dalla protezione del documento. La protezione da scrittura è specificata in Microsoft Word nelle opzioni della finestra di dialogo Salva con nome.

Non è possibile creare istanze di questa classe direttamente. È possibile accedere alle impostazioni di protezione del documento tramite[`WriteProtection`](../../aspose.words/document/writeprotection/) proprietà.

## Esempi

Mostra come proteggere un documento con una password.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Inserisci una password lunga fino a 15 caratteri, quindi verifica lo stato di protezione del documento.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// La protezione non impedisce che il documento venga modificato a livello di programmazione, né ne crittografa il contenuto.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
