---
title: Document.WriteProtection
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Fornisce laccesso alle opzioni di protezione da scrittura del documento.
type: docs
weight: 500
url: /it/net/aspose.words/document/writeprotection/
---
## Document.WriteProtection property

Fornisce l'accesso alle opzioni di protezione da scrittura del documento.

```csharp
public WriteProtection WriteProtection { get; }
```

### Esempi

Mostra come proteggere un documento con una password.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Immettere una password lunga fino a 15 caratteri, quindi verificare lo stato di protezione del documento.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// La protezione non impedisce la modifica del documento a livello di codice, né ne crittografa il contenuto.
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
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


