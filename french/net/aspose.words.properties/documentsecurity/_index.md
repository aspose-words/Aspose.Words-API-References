---
title: Enum DocumentSecurity
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Properties.DocumentSecurity énumération. Utilisé comme valeur pour leSecurity property. Spécifie le niveau de sécurité dun document sous forme de valeur numérique.
type: docs
weight: 4490
url: /fr/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Utilisé comme valeur pour le[`Security`](../builtindocumentproperties/security/) property. Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

```csharp
[Flags]
public enum DocumentSecurity
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucun état de sécurité n'est spécifié par la propriété. |
| PasswordProtected | `1` | Le document est protégé par mot de passe. (La note n'a jamais été vue dans un document jusqu'à présent). |
| ReadOnlyRecommended | `2` | Le document à ouvrir en lecture seule si possible, mais le paramètre peut être remplacé. |
| ReadOnlyEnforced | `4` | Le document à toujours ouvrir en lecture seule. |
| ReadOnlyExceptAnnotations | `8` | Le document doit toujours être ouvert en lecture seule sauf pour les annotations. |

### Exemples

Montre comment utiliser les propriétés du document pour afficher le niveau de sécurité d'un document.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Si nous configurons un document en lecture seule, il affichera cet état en utilisant la propriété intégrée "Sécurité".
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Protégez en écriture un document, puis vérifiez son niveau de sécurité.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "Sécurité" est une propriété descriptive. Nous pouvons modifier sa valeur manuellement.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Voir également

* espace de noms [Aspose.Words.Properties](../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../)


