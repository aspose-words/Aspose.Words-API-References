---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.DocumentSecurity per migliorare la sicurezza dei tuoi documenti. Specifica e gestisci facilmente i livelli di sicurezza per una protezione ottimale.
type: docs
weight: 5220
url: /it/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Utilizzato come valore per il[`Security`](../builtindocumentproperties/security/) property. Specifica il livello di sicurezza di un documento come valore numerico.

```csharp
[Flags]
public enum DocumentSecurity
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Non ci sono stati di sicurezza specificati dalla proprietà. |
| PasswordProtected | `1` | Il documento è protetto da password. (La nota non è mai stata vista finora in un documento). |
| ReadOnlyRecommended | `2` | Se possibile, il documento deve essere aperto in sola lettura, ma l'impostazione può essere ignorata. |
| ReadOnlyEnforced | `4` | Il documento deve essere sempre aperto in sola lettura. |
| ReadOnlyExceptAnnotations | `8` | Il documento deve essere sempre aperto in sola lettura, ad eccezione delle annotazioni. |

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

* spazio dei nomi [Aspose.Words.Properties](../../aspose.words.properties/)
* assemblea [Aspose.Words](../../)
