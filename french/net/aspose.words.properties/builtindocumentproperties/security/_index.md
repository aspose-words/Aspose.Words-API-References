---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words pour .NET
description: Découvrez la fonctionnalité de sécurité BuiltInDocumentProperties, qui définit précisément le niveau de sécurité de vos documents. Améliorez la protection de vos documents dès aujourd'hui !
type: docs
weight: 270
url: /fr/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

```csharp
public DocumentSecurity Security { get; set; }
```

## Remarques

Utilisez cette propriété à titre informatif uniquement, car Microsoft Word ne la définit pas toujours. Cette propriété est disponible uniquement dans les documents DOC et OOXML.

Pour protéger ou déprotéger un document, utilisez the [`Protect`](../../../aspose.words/document/protect/) et[`Unprotect`](../../../aspose.words/document/unprotect/) méthodes.

Aspose.Words met à jour cette propriété avec une valeur correcte avant d'enregistrer un document.

## Exemples

Montre comment utiliser les propriétés du document pour afficher le niveau de sécurité d'un document.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Si nous configurons un document pour qu'il soit en lecture seule, il affichera ce statut à l'aide de la propriété intégrée « Sécurité ».
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

// « Sécurité » est une propriété descriptive. Nous pouvons modifier sa valeur manuellement.
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
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
