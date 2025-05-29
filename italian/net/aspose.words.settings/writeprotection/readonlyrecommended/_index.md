---
title: WriteProtection.ReadOnlyRecommended
linktitle: ReadOnlyRecommended
articleTitle: ReadOnlyRecommended
second_title: Aspose.Words per .NET
description: Scopri la proprietà WriteProtection ReadOnlyRecommended, che guida gli utenti ad aprire i documenti in modalità di sola lettura per una maggiore sicurezza e integrità.
type: docs
weight: 20
url: /it/net/aspose.words.settings/writeprotection/readonlyrecommended/
---
## WriteProtection.ReadOnlyRecommended property

Specifica se l'autore del documento ha raccomandato di aprirlo in sola lettura.

```csharp
public bool ReadOnlyRecommended { get; set; }
```

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

* class [WriteProtection](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
