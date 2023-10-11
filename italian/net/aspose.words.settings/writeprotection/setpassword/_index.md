---
title: WriteProtection.SetPassword
second_title: Aspose.Words per .NET API Reference
description: WriteProtection metodo. Imposta la password di protezione da scrittura per il documento.
type: docs
weight: 30
url: /it/net/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method

Imposta la password di protezione da scrittura per il documento.

```csharp
public void SetPassword(string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | String | La password da impostare. Non può essere`nullo`, ma può essere una stringa vuota. |

### Osservazioni

Se è impostata una password, Microsoft Word richiederà all'utente di inserirla o di aprire il documento in sola lettura.

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


