---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words pour .NET
description: Découvrez la protection active des documents pour une sécurité et une intégrité des données renforcées. Protégez vos fichiers en toute simplicité grâce à nos fonctionnalités avancées.
type: docs
weight: 340
url: /fr/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Obtient le type de protection de document actuellement actif.

```csharp
public ProtectionType ProtectionType { get; }
```

## Remarques

Cette propriété permet de récupérer le type de protection du document actuellement défini. Pour modifier le type de protection du document, utilisez le[`Protect`](../protect/) et[`Unprotect`](../unprotect/) méthodes.

Lorsqu'un document est protégé, l'utilisateur ne peut effectuer que des modifications limitées, telles que l'ajout d'annotations, la réalisation de révisions ou le remplissage d'un formulaire.

Notez que la protection des documents est différente de la protection en écriture. La protection en écriture est spécifiée à l'aide de[`WriteProtection`](../writeprotection/)

## Exemples

Montre comment protéger et déprotéger un document.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Si nous ouvrons ce document avec Microsoft Word dans l’intention de le modifier,
// nous devrons appliquer le mot de passe pour passer la protection.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Notez que la protection s'applique uniquement aux utilisateurs de Microsoft Word ouvrant notre document.
// Nous n'avons en aucun cas chiffré le document et nous n'avons pas besoin du mot de passe pour l'ouvrir et le modifier par programmation.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Il existe deux manières de supprimer la protection d'un document.
// 1 - Sans mot de passe :
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Avec le bon mot de passe :
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Voir également

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
