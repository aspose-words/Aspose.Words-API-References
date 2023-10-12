---
title: WriteProtection.ValidatePassword
second_title: Aspose.Words per .NET API Reference
description: WriteProtection metodo. RestituisceVERO se la password specificata è la stessa password di protezione da scrittura con cui il documento è stato protetto. Se il documento non è protetto da scrittura con password restituiscefalso .
type: docs
weight: 40
url: /it/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Restituisce`VERO` se la password specificata è la stessa password di protezione da scrittura con cui il documento è stato protetto. Se il documento non è protetto da scrittura con password restituisce`falso` .

```csharp
public bool ValidatePassword(string password)
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

* class [WriteProtection](../)
* spazio dei nomi [Aspose.Words.Settings](../../writeprotection/)
* assemblea [Aspose.Words](../../../)


