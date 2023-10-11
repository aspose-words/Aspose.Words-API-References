---
title: BuiltInDocumentProperties.Security
second_title: Aspose.Words per .NET API Reference
description: BuiltInDocumentProperties proprietà. Specifica il livello di sicurezza di un documento come valore numerico.
type: docs
weight: 250
url: /it/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Specifica il livello di sicurezza di un documento come valore numerico.

```csharp
public DocumentSecurity Security { get; set; }
```

### Osservazioni

Utilizzare questa proprietà solo a scopo informativo poiché Microsoft Word non imposta sempre questa proprietà. Questa proprietà è disponibile solo nei documenti DOC e OOXML.

Per proteggere o rimuovere la protezione di un documento utilizzare [`Protect`](../../../aspose.words/document/protect/) E[`Unprotect`](../../../aspose.words/document/unprotect/) metodi.

Aspose.Words aggiorna questa proprietà su un valore corretto prima di salvare un documento.

### Esempi

Mostra come utilizzare le proprietà del documento per visualizzare il livello di sicurezza di un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Se configuriamo un documento come di sola lettura, visualizzerà questo stato utilizzando la proprietà integrata "Sicurezza".
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

// "Sicurezza" è una proprietà descrittiva. Possiamo modificare il suo valore manualmente.
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
* spazio dei nomi [Aspose.Words.Properties](../../builtindocumentproperties/)
* assemblea [Aspose.Words](../../../)


