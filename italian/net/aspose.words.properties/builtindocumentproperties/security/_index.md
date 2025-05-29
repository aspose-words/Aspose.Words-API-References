---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words per .NET
description: Scopri la funzionalità di sicurezza BuiltInDocumentProperties, che definisce con precisione il livello di sicurezza dei tuoi documenti. Migliora la protezione dei tuoi documenti oggi stesso!
type: docs
weight: 270
url: /it/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Specifica il livello di sicurezza di un documento come valore numerico.

```csharp
public DocumentSecurity Security { get; set; }
```

## Osservazioni

Utilizzare questa proprietà solo a scopo informativo perché Microsoft Word non la imposta sempre. Questa proprietà è disponibile solo nei documenti DOC e OOXML.

Per proteggere o rimuovere la protezione da un documento utilizzare the [`Protect`](../../../aspose.words/document/protect/) E[`Unprotect`](../../../aspose.words/document/unprotect/) metodi.

Aspose.Words aggiorna questa proprietà con un valore corretto prima di salvare un documento.

## Esempi

Mostra come utilizzare le proprietà del documento per visualizzare il livello di sicurezza di un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Se configuriamo un documento come di sola lettura, questo stato verrà visualizzato tramite la proprietà integrata "Sicurezza".
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Proteggere da scrittura un documento e quindi verificarne il livello di sicurezza.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "Security" è una proprietà descrittiva. Possiamo modificarne il valore manualmente.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Guarda anche

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
