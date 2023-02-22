---
title: BuiltInDocumentProperties.Security
second_title: Référence de l'API Aspose.Words pour .NET
description: BuiltInDocumentProperties propriété. Spécifie le niveau de sécurité dun document sous forme de valeur numérique.
type: docs
weight: 250
url: /fr/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

```csharp
public DocumentSecurity Security { get; set; }
```

### Remarques

Utilisez cette propriété à des fins d'information uniquement car Microsoft Word ne définit pas toujours cette propriété. Cette propriété est disponible uniquement dans les documents DOC et OOXML.

Pour protéger ou déprotéger un document, utilisez the [`Protect`](../../../aspose.words/document/protect/) et[`Unprotect`](../../../aspose.words/document/unprotect/)méthodes.

Aspose.Words met à jour cette propriété avec une valeur correcte avant d'enregistrer un document.

### Exemples

Montre comment utiliser les propriétés du document pour afficher le niveau de sécurité d'un document.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Si nous configurons un document en lecture seule, il affichera cet état à l'aide de la propriété intégrée "Security".
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Protégez un document en écriture, puis vérifiez son niveau de sécurité.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "Security" est une propriété descriptive. Nous pouvons modifier sa valeur manuellement.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Voir également

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../builtindocumentproperties/)
* Assemblée [Aspose.Words](../../../)


