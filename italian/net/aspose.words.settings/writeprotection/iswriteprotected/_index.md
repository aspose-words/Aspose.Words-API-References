---
title: WriteProtection.IsWriteProtected
linktitle: IsWriteProtected
articleTitle: IsWriteProtected
second_title: Aspose.Words per .NET
description: Scopri la proprietà WriteProtection IsWriteProtected e controlla facilmente se è attiva una password di protezione da scrittura per una maggiore sicurezza e integrità dei dati.
type: docs
weight: 10
url: /it/net/aspose.words.settings/writeprotection/iswriteprotected/
---
## WriteProtection.IsWriteProtected property

Restituisce`VERO` quando è impostata una password di protezione da scrittura.

```csharp
public bool IsWriteProtected { get; }
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
