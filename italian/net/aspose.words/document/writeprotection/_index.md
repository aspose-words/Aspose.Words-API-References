---
title: Document.WriteProtection
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words per .NET
description: Esplora la proprietà Document WriteProtection per gestire senza sforzo le impostazioni di protezione da scrittura dei tuoi documenti e migliorarne la sicurezza.
type: docs
weight: 520
url: /it/net/aspose.words/document/writeprotection/
---
## Document.WriteProtection property

Fornisce accesso alle opzioni di protezione da scrittura del documento.

```csharp
public WriteProtection WriteProtection { get; }
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

* class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
